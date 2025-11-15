# UNWSP-Python-Week-11
Instructions:
Program #1:
Create a GUI window that displays your favorite saying.
#Braden Phetsarath
#11/11
#Instructions: Program #1: Create a GUI window that displays your favorite saying.

from tkinter import *
class Gui:
    def __init__(self):
        self.window = Tk()

        self.window.title("My favorite Saying")
        self.label = Label(self.window,text = 'A jack of all trades is a master of none, but oftentimes is better than a master of one.', font = ('Arial', 20))
        self.label.pack()

        self.window.mainloop()

if __name__ == "__main__":
    my_gui= Gui()

Program #2: 
Write a GUI program that displays your name and address when a "Show Info" button is clicked.  There should also be a "Quit" button which exists the GUI.

#Braden Phetsarath
#11/12
#Program #2: Write a GUI program that displays your name and address when a "Show Info" button is clicked. There should also be a "Quit" button which exists the GUI.

from tkinter import *

class Gui:
    def __init__(self):
        self.window = Tk()
        self.window.geometry("400x300") 
        self.window.title("Gui")

     
        self.button1 = Button(
            self.window,
            text="Show Info",
            fg="orange",
            command=self.show_info
        )
        self.button1.pack(side=left, padx=20, pady=20)

      
        self.button2 = Button(
            self.window,
            text="Quit",
            fg="red",
            command=self.window.destroy
        )
        self.button2.pack(side=right, padx=20, pady=20)

        # Label for displaying information
        self.info_label = Label(
            self.window,
            text="Info will appear here",
            font=("Arial", 12),
            wraplength=300,
            justify="center"
        )
        self.info_label.pack(pady=40)

        self.window.mainloop()

    def show_info(self):

        self.info_label.config(
            text="Braden Phetsarath\n2014 Foresthills Drive\nSpringfield, IL 62704"
        )

if __name__ == "__main__":
    Gui()
