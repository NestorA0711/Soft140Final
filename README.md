# Soft140Final
#Final project
from tkinter import *
from tkinter import ttk 
from tkinter import messagebox


root = Tk()
#root.title('Codemy.com - Currenry Conversion')
#root.iconbitmap('c:/gui/codemy.ico')
root.geometry('500x500')

#create tabs
myNotebook = ttk.Notebook(root)
myNotebook.pack(pady=5)

#create two frames 
currencyFrame = Frame(myNotebook, width = 480, height = 480)
conversionFrame = Frame(myNotebook, width = 480, height = 480)

currencyFrame.pack(fill='both',expand=1)
conversionFrame.pack(fill='both',expand=1)

#add tabs
myNotebook.add(currencyFrame, text="Currencies")
myNotebook.add(conversionFrame, text="Covert")

"""CURRENCY
INFORMATION 
"""
def lock():
    pass

def unlock():
    pass

home = LabelFrame(currencyFrame, text='Your Home Currency')
home.pack(pady=20)

#home currency entry box
HomeEntry = Entry(home, font =("Helvetica, 24"))
HomeEntry.pack(pady=10 , padx=10)

#conversion currency frame
conversion = LabelFrame(currencyFrame, text="Conversion Currency")
conversion.pack(pady=20)

#convert to label
conversionLabel = Label(conversion,text="Currency to Convert To...")
conversionLabel.pack(pady=10)

#covert to entry 
conversionEntry = Entry(conversion, font=("Helvetica,24"))
conversionEntry.pack(pady=10, padx=10)

#rate label
rateLabel = Label(conversion,text="Currency to Convert To...")
rateLabel.pack(pady=10)

#rate entry
rateEntry = Entry(conversion, font=("Helvetica,24"))
rateEntry.pack(pady=10, padx=10)

#button frame
buttonFrame = Frame(currencyFrame)
buttonFrame.pack(pady=20)

#create buttons
lockbutton = Button(buttonFrame, text="Lock", command=lock)
lockbutton.grid(row=0, column=0, padx=10)

unlockbutton = Button(buttonFrame, text="Unlock", command=unlock)
unlockbutton.grid(row=0, column=1, padx=10)

root.mainloop()
