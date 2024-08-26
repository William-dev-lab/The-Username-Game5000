
import time
import random

print("Welcome to The Username Game!👋")
username = input("Please enter a username: 🏷️ ")

# Simulate checking the username
print("Checking username...👨🏻‍💻")
time.sleep(1.5)
print("Username already taken.")
time.sleep(1)

# Loop until a valid username is provided
while True:
    username = input("Enter a new username (not asking) ▄︻デ══━一💥: ")
    print("Checking username... 👨🏻‍💻")
    time.sleep(1.5)
    length = len(username)
    if length < 4:
        print("Is that a username or a secret code? Try at least 4 characters! 🔐")
    elif not any(char in username for char in "!@#$%^&*()"):
        print("Your username needs to sparkle! Add some special characters! ✨")
    elif sum(1 for char in username if char in "aeiou") < 2:
        print("Your username is missing vowels! Are you a robot? 🤖")
    elif not any(char.isdigit() for char in username):
        print("No numbers? Is this a username or a word? Add some digits! 🔢")
    elif "💩" not in username:
        print("Where's the poop emoji? It’s essential for a perfect username! 💩")
    elif username.lower() in ["admin", "root", "username"]:
        print("Classic! But not allowed. Try something more unique! 🔑")
    else:
        print("Congrats🎉!You have beat The Username Game!")
