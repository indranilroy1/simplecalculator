import tkinter as tk
from tkinter import *
import webbrowser
root=tk.Tk()
root.geometry('500x200')



def calculator():
   a=int(e1.get())
   b=int(e2.get())
   c=a+b
   txtvr.set(c)
def sub():
   e=int(e1.get())
   g=int(e2.get())
   h=e-g
   txtvr.set(h)
def mul():
   f=int(e1.get())
   i=int(e2.get())
   j=f*i
   txtvr.set(j)
def div():
   k=int(e1.get())
   l=int(e2.get())
   m=k/l
   txtvr.set(m)





txtvr=StringVar()
Label(root,text="Give First Number").grid(row=0,column=0)
Label(root,text="Give Second Number").grid(row=1,column=0)
Label(root,text="Result").grid(row=3,column=0)
result=Label(root,text=" ",textvariable=txtvr).grid(row=3,column=1)

e1= Entry(root)
e2= Entry(root)
e1.grid(row=0,column=1)
e2.grid(row=1,column=1)

Button(root,text="Add",bd='15',bg="orange",command=calculator).grid(row = 5,column=0,pady=0,padx=4)
Button(root,text="Multipy",bd='15',bg="blue",command=mul).grid(row=6,column=0,pady=1,padx=5)
Button(root,text="Sub",bd='15',bg="green",command=sub).grid(row=7,column=0,pady=0,padx=5)
Button(root,text="Divide",bd='15',bg="red",command=div).grid(row=8,column=0,pady=10,padx=7)

root.mainloop()
