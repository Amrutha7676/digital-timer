# digital-timer
import tkinter as tk
from time import strftime

# Create the main window
root = tk.Tk()
root.title("Digital Clock")

# Create a label to display the time
clock_label = tk.Label(root, font=('Arial', 60), bg='black', fg='lime')
clock_label.pack(anchor='center')

# Define the function to update time
def update_time():
    current_time = strftime('%H:%M:%S')
    clock_label.config(text=current_time)
    root.after(1000, update_time)  # call this function again in 1 second

# Call the function once to start
update_time()

# Run the app
root.mainloop()
