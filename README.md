# Password-generator

import random
import string

passLength = int(input("How long do you want your password to be? "))

if passLength == 6:

    letters = int(input("How many letters do you want on your password? "))
    numbers = int(input("How many numbers do you want on your password? "))
    symbols = int(input("How many characters do you want on your password? "))

    if (letters + numbers + symbols) == 6:

        passWord = [random.choice(string.ascii_letters) for word in range(letters)]
        passNum = [random.choice(string.digits) for dig in range(numbers)]
        passChar = [random.choice(string.punctuation) for punc in range(symbols)]
        passGen = ''.join(passWord + passNum + passChar)
        passGenerator = ''.join(random.choice(passGen) for len in range(passLength))
        print("Your password is " + str(passGenerator))

    else:
        print("Your input lengths are > 6")

else:
    print("Your chosen length is > 6")

