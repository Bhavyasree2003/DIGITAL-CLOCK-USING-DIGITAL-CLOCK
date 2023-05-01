"""Code For Digtal Clock with GUI with TKinter"""
# importing whole module 
import time
from tkinter import *
# creating tkinter window 
root = Tk()
root.title("Digital Clock")
root.resizable()
lbl = Label(root)
lbl.grid(row=0, column=0)
# This function is used to 
# display time on the label
def display():
    time_get = time.strftime("%Y/%m/%d\n%I:%M:%S %p")
    lbl.config(text=time_get, bg='black', fg='white',
               font=('Times New Roman', 50, 'bold'))
    lbl.after(100, display)
display()
root.mainloop()

