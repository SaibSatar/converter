from tkinter import*


#tkinter_design
window=Tk()
enter=Entry(window,font=('Bnazanin',20,'bold'),bg='white',bd=10)
enter.grid(row=1,column=0,columnspan=4)

#functions

def convert_bin():
        try:
            global value
            value=int((enter.get()))
            bv=bin(value)
            enter.delete(0,END)
            enter.insert(0,bv)
        except:
              enter.delete(0,END)
              enter.insert(0,bin(value))


def convert_oct():
        try:
            global value
            value=int((enter.get()))
            ov=oct(value)
            enter.delete(0,END)
            enter.insert(0,ov)
        except:
              enter.delete(0,END)
              enter.insert(0,oct(value))

                
def convert_hex():
      try:
            global value
            value=int((enter.get()))
            oh=hex(value)
            enter.delete(0,END)
            enter.insert(0,oh)
      except:
              enter.delete(0,END)
              enter.insert(0,hex(value))

def convert_dec():
      try:
            global value
            enter.delete(0,END)
            enter.insert(0,value)
      except:
            enter.delete(0,END)
            enter.insert(value)
              
    
   

#Buttons

""" dec """
but_dec=Button(window,font=('Bnazanin',20,'bold'),text='dec',command=convert_dec)
but_dec.grid(row=2,column=0,sticky=W,padx=10,pady=20)

""" bin """
but_bin=Button(window,font=('Bnazanin',20,'bold'),text='bin',command=convert_bin)
but_bin.grid(row=2,column=0,sticky=E,padx=100,pady=20)

"""oct"""
but_oct=Button(window,font=('Bnazanin',20,'bold'),text='oct',command=convert_oct)
but_oct.grid(row=2,column=1,sticky=E,padx=10,pady=20)

"""hex"""
but_hex=Button(window,font=('Bnazanin',20,'bold'),text='hex',command=convert_hex)
but_hex.grid(row=2,column=1,sticky=W,padx=100,pady=20)


window.mainloop()
