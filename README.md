# CODESOF03
import random
import string

def generate_password(length):
    password = []
    password.append(random.choice(string.ascii_lowercase))
    password.append(random.choice(string.ascii_uppercase))
    password.append(random.choice(string.digits))
    password.append(random.choice(string.punctuation))

    for i in range(length - 4):
        password.append(random.choice(string.ascii_letters + string.digits + string.punctuation))

    random.shuffle(password)
    return ''.join(password)

def main():
    print("Random Password Generator")
    length = int(input("Enter the length of the password (min 4): "))
    if length < 4:
        print("Password length should be at least 4 characters.")
    else:
        password = generate_password(length)
        print("Generated Password : ", password)

if __name__ == "__main__":
    main()
    
