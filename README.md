# Automated-WhatsApp
Automated WhatsApp
import tkinter as tk
import pywhatkit as kit

def sendmsg():
     global name
     global text
     global time_h
     global time_m
     num=x.get()
     text=y.get()
     time_h=th.get()
     time_m=tm.get()
     root.destroy()
     kit.sendwhatmsg(num,text,time_h,time_m)



root = tk.Tk()
root.configure(bg="black")
x=tk.StringVar()
y=tk.StringVar()
th=tk.IntVar()
tm=tk.IntVar()
root.geometry("300x200")
root.title("WhatsApp GUI")
label1= tk.Label(root,text="Enter Your Number").grid(row=0,column=0)
label2= tk.Label(root,text="Enter Your Text").grid(row=1,column=0)
label3= tk.Label(root,text="Enter Your Time in Hour").grid(row=2,column=0)
label4= tk.Label(root,text="Enter Your Time in minute").grid(row=3,column=0)

entry1=tk.Entry(root,textvariable=x,bg="royal blue").grid(row=0,column=1)
entry2=tk.Entry(root,textvariable=y,bg="royal blue").grid(row=1,column=1)
entry3=tk.Entry(root,textvariable=tm,bg="royal blue").grid(row=2,column=1)
entry4=tk.Entry(root,textvariable=th,bg="royal blue").grid(row=3,column=1)

button=tk.Button(root,text="Send",command=sendmsg).grid(row=5,column=1)

root.mainloop()
