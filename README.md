from tkinter import *

formdangki=Tk()
formdangki.title('TEST')
formdangki.geometry('500x500')


username = StringVar()
password = StringVar()
date =  StringVar()
nations = StringVar()
email = StringVar()
hovaten = StringVar()
list=['Vietnam','China','Japan','Korea']
droplist=OptionMenu(formdangki, nations, *list)
nations.set('Country')

Title=Label(formdangki, text ="ĐĂNG KÍ", font=("Time New Roman", 16, "bold"), fg="green")
Title.pack()

# hovaten
hovaten_lable=Label(formdangki, text ="Họ và tên của bạn")
hovaten_lable.pack()
hovaten_lable.place(x=15, y=20)

hovatenEntry=Entry(formdangki, textvariable=hovaten)
hovatenEntry.pack()
hovatenEntry.place(x=15, y=42)

# username
username_lable=Label(formdangki, text ="Username")
username_lable.pack()
usernameEntry=Entry(formdangki, textvariable=username)
usernameEntry.pack()

# password
Password_lable=Label(formdangki, text ="Password")
Password_lable.pack()
PasswordEntry=Entry(formdangki, textvariable=password)
PasswordEntry.pack()

#date
date_lable=Label(formdangki, text ="Ngày tháng năm sinh")
date_lable.pack()
date_entry=Entry(formdangki, textvariable=date)
date_entry.pack()

#email
email_lable=Label(formdangki, text ="Email")
email_lable.pack()
email_entry=Entry(formdangki, textvariable=email)
email_entry.pack()

nations.set('Quoc tich')
droplist.config(width=7, font=('Times New  Roman', 10))
droplist.place(x=150, y=250)

formdangki.mainloop()
