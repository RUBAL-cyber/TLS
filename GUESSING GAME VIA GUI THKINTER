import tkinter as tk
from tkinter import messagebox
import random

# Function to check if the user's guess is correct
def check_guess():
    try:
        guess = int(guess_entry.get())
        if guess == secret_number:
            messagebox.showinfo("Congratulations!", "You guessed the correct number!")
        elif guess < secret_number:
            messagebox.showwarning("Too Low", "Try a higher number.")
        else:
            messagebox.showwarning("Too High", "Try a lower number.")
    except ValueError:
        messagebox.showerror("Invalid Input", "Please enter a valid number.")

# Function to start a new game
def new_game():
    global secret_number
    secret_number = random.randint(1, 100)
    guess_entry.delete(0, 'end')

# Create the main window
root = tk.Tk()
root.title("Number Guessing Game")

# Create and place widgets
title_label = tk.Label(root, text="Guess the Number Game", font=("Helvetica", 16))
title_label.pack(pady=10)

instruction_label = tk.Label(root, text="Enter a number between 1 and 100:")
instruction_label.pack()

guess_entry = tk.Entry(root)
guess_entry.pack()

check_button = tk.Button(root, text="Check Guess", command=check_guess)
check_button.pack()

new_game_button = tk.Button(root, text="New Game", command=new_game)
new_game_button.pack()

# Initialize the secret number
secret_number = random.randint(1, 100)

# Start the GUI main loop
root.mainloop()
