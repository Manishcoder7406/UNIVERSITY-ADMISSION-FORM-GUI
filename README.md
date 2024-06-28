# UNIVERSITY-ADMISSION-FORM-GUI-PROJECT
from tkinter import *
root= Tk()
root.geometry("555x600")
root.title("ADMISSION FORM")

def getvals():
    print("entries entered")

def mypack():
    pass 

label=Label(root,text="WELCOME TO CT UNIVERSITY",font="lucida 15 bold",relief=SUNKEN,bg="sky blue",borderwidth=5)
label.grid(row=0,column=3)

admis=Label(root,text="ADMISSIONS OPEN",bg="grey",font="lucida 13 bold",relief=GROOVE,borderwidth=3)
admis.grid(row=1,column=3)

Label(root,text="FILL YOUR DETAILS",font="lucida 15 bold",padx=12,pady=14).grid(row=3,column=3)
 

#detais from user we need 
name=Label(root,text="NAME")
marks=Label(root,text="MARKS IN 12")
marks2=Label(root,text="MARKS IN 10")
contact=Label(root,text="CONTACT NO.")
resi=Label(root,text="RESIDENCE")
field=Label(root,text="COURSE WANT")

name.grid(row=6,column=2)
marks.grid(row=7,column=2)
marks2.grid(row=8,column=2)
contact.grid(row=9,column=2)
resi.grid(row=10,column=2)
field.grid(row=11,column=2)

namevalue=StringVar()
marksvalue=StringVar()
marks2value=StringVar()
contactvalue=StringVar()
resivalue=StringVar()
fieldvalue=StringVar()
check=StringVar()

nameentry=Entry(root,textvariable=namevalue)
marksentry=Entry(root,textvariable=marksvalue)
marks2entry=Entry(root,textvariable=marks2value)
contactentry=Entry(root,textvariable=contactvalue)
resientry=Entry(root,textvariable=resivalue)
fieldentry=Entry(root,textvariable=fieldvalue)

nameentry.grid(row=6,column=3)
marksentry.grid(row=7,column=3)
marks2entry.grid(row=8,column=3)
contactentry.grid(row=9,column=3)
resientry.grid(row=10,column=3)
fieldentry.grid(row=11,column=3)


check2=Checkbutton(text="Want special IBM courses ?",variable=check)
check2.grid(row=12,column=3)

Button(text="SUBMIT",command=getvals).grid(row=13,column=3)

var=IntVar()
Label(root,text="CHOOSE THE SCHOOL PROVIDED BY UNIVERSITY",font="lucida 13 bold",justify=LEFT).grid(row=15,column=3)
radio=Radiobutton(root,text="SCHOOL OF ENGINEERING",variable=var,value=1,padx=14).grid(row=16,column=2)
radio=Radiobutton(root,text="SCHOOL OF MANAGEMENT ",variable=var,value=2,padx=14).grid(row=17,column=2)
radio=Radiobutton(root,text="SCHOOL OF PARAMEDICAL",variable=var,value=3,padx=14).grid(row=18,column=2)
radio=Radiobutton(root,text="SCHOOL OF LAW        ",variable=var,value=4,padx=14).grid(row=19,column=2)
radio=Radiobutton(root,text="SCHOOL OF AIRLINES   ",variable=var,value=5,padx=14).grid(row=20,column=2)
radio=Radiobutton(root,text="HOTEL MANAGEMENT     ",variable=var,value=6,padx=14).grid(row=21,column=2)
radio=Radiobutton(root,text="FASHION DESIGNING    ",variable=var,value=7,padx=14).grid(row=22,column=2)
radio=Radiobutton(root,text="SCHOOL OF MULTIMEDIA  ",variable=var,value=8,padx=14).grid(row=23,column=2)
radio=Radiobutton(root,text="SCHOOL OF AGRICULTURE ",variable=var,value=9,padx=14).grid(row=24,column=2)

Button(text="SUBMIT",command=getvals).grid(row=25,column=3)


scroll=Scrollbar(root)
scroll.grid(row=0,column=0)
listbox=Listbox(root,yscrollcommand=scroll.set)
for i in range (344):
    listbox.insert(END,f"item{i}")
scroll.config(command=listbox.yview)


 
mymenu=Menu(root)
m1=Menu(mymenu,tearoff=0)
m1.add_command(label="SCHOOL OF ENGINEERING")
m1.add_command(label="SCHOOL OF MANAGEMENT")
m1.add_command(label="SCHOOL OF PARAMEDICAL")
m1.add_command(label="SCHOOL OF LAW")
m1.add_command(label="SCHOOL OF AIRLINES")
m1.add_command(label="HOTEL MANAGEMENT")
root.config(menu=mymenu)
mymenu.add_cascade(label="FACULTY",menu=m1)
mymenu.add_command(label="PACKAGES",command=mypack)
mymenu.add_command(label="DETAILS",command=quit)
mymenu.add_command(label="INFRASTRUCTURE",command=quit)
mymenu.add_command(label="RESULTS",command=quit)
root.config(menu=mymenu)


























#statusbar
#statusvar=StringVar()
#statusvar.set("CT UNIVERSITY  IS  A  PRESTIGEOUS  INSTITUTE  IN  THE  FIELD  OF  EXCELLENCE")
#sbar=Label(root,textvariable=statusvar,relief=SUNKEN,anchor="center")
#sbar.pack(side=BOTTOM,fill=X)

root.mainloop()
