# Calculator
from tkinter import *

mw=Tk()

mw.title("Calculator")
#Operations are performed when we clicked on button's

#mw.geometry('400x400')..............................................................>

def clear():
    block.delete(0, END)
    
def click(num):
    cur_num = block.get()
    clear()
    f_num = cur_num + num
    block.insert(0, f_num)

def equal():
    res=eval(str(block.get()))
    clear()
    block.insert(0, res)

#Creating Button's

l=Label(mw,text='JK CALCULATOR',font=("Arial",20))

block=Entry(mw,width=27,justify=RIGHT,bg='black',fg='white',font=('Arial',16))
btn_per=Button(mw,text='%',padx=27,pady=5,bg='black',font=('Arial',14),fg='white',command=lambda :click('%'))
btn_div=Button(mw,text='/',padx=33,pady=5,bg='black',font=('Arial',14),fg='white',command=lambda :click('/'))
btn_mul=Button(mw,text='*',padx=33,pady=5,bg='black',font=('Arial',14),fg='white',command=lambda :click('*'))
btn_poi=Button(mw,text='.',padx=21,pady=5,bg='black',font=('Arial',14),fg='white',command=lambda :click('.'))

btn_7=Button(mw,text='7',padx=30,pady=5,bg='black',font=('Arial',14),fg='white',command=lambda :click('7'))
btn_8=Button(mw,text='8',padx=30,pady=5,bg='black',font=('Arial',14),fg='white',command=lambda :click('8'))
btn_9=Button(mw,text='9',padx=31,pady=5,bg='black',font=('Arial',14),fg='white',command=lambda :click('9'))
btn_sub=Button(mw,text='-',padx=20,pady=5,bg='black',font=('Arial',14),fg='white',command=lambda :click('-'))

btn_4=Button(mw,text='4',padx=30,pady=5,bg='black',font=('Arial',14),fg='white',command=lambda :click('4'))
btn_5=Button(mw,text='5',padx=30,pady=5,bg='black',font=('Arial',14),fg='white',command=lambda :click('5'))
btn_6=Button(mw,text='6',padx=31,pady=5,bg='black',font=('Arial',14),fg='white',command=lambda :click('6'))
btn_add=Button(mw,text='+',padx=17,pady=28,bg='black',font=('Arial',15),fg='white',command=lambda :click('+'))

btn_1=Button(mw,text='1',padx=30,pady=5,bg='black',font=('Arial',14),fg='white',command=lambda :click('1'))
btn_2=Button(mw,text='2',padx=30,pady=5,bg='black',font=('Arial',14),fg='white',command=lambda :click('2'))
btn_3=Button(mw,text='3',padx=31,pady=5,bg='black',font=('Arial',14),fg='white',command=lambda :click('3'))

btn_ac=Button(mw,text='CLEAR',padx=3,pady=5,bg='black',font=('Arial',14),fg='white',command=clear)
btn_0=Button(mw,text='0',padx=30,pady=5,bg='black',font=('Arial',14),fg='white',command=lambda :click('0'))
btn_equ=Button(mw,text='=',padx=63,pady=5,bg='black',font=('Arial',14),fg='white',command=equal)

note=Label(mw,text="NOTE : Ensure the operation's are to be performed\n in the calculator are Valid, Otherwise it will produce\n an in-accurate result's")

#Showing Button's

l.grid(row=0,columnspan=4)

block.grid(row=1,column=0,columnspan=4,pady=8)
btn_per.grid(row=2,column=0)
btn_div.grid(row=2,column=1)
btn_mul.grid(row=2,column=2)
btn_poi.grid(row=2,column=3)

btn_7.grid(row=3,column=0)
btn_8.grid(row=3,column=1)
btn_9.grid(row=3,column=2)
btn_sub.grid(row=3,column=3)

btn_4.grid(row=4,column=0)
btn_5.grid(row=4,column=1)
btn_6.grid(row=4,column=2)
btn_add.grid(row=4,column=3,rowspan=2)

btn_1.grid(row=5,column=0)
btn_2.grid(row=5,column=1)
btn_3.grid(row=5,column=2)

btn_ac.grid(row=6,column=0)
btn_0.grid(row=6,column=1)
btn_equ.grid(row=6,column=2,columnspan=2)

note.grid(row=7,columnspan=4)

mw.mainloop()
