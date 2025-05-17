code_target = ""
temp_target = ""
pastguess = []
win = 0
point = 0
lives = 6
progress = [R'''
  +---+
  |   |
  O   |
 /|\  |
 / \  |
      |
=========''',R'''

  +---+
  |   |
  O   |
 /|\  |
 /    |
      |
=========''',R'''
  +---+
  |   |
  O   |
 /|\  |
      |
      |
=========''',R'''
  +---+
  |   |
  O   |
 /|   |
      |
      |
=========''',R'''
  +---+
  |   |
  O   |
  |   |
      |
      |
=========''',R'''
  +---+
  |   |
  O   |
      |
      |
      |
=========''',R'''
  +---+
  |   |
      |
      |
      |
      |
=========''']








print("***WELCOME TO HANGMAN***\n")

def validate(subject):
    for i in subject:
        if not i.isalpha():
            print("The word must not contain any numbers or special characters. Try again.")
            return False
    return True 

while True:
    word = input("Player 1, enter your word: ").lower()
    if validate(word):
        break

for i in range(len(word)): code_target = code_target + "?"
print(code_target)

print(f"\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\nPlayer 1 has selected the word.\n\n{code_target}")


def attempt(guess,x):
    global temp_target
    global code_target
    global point
    global lives
    global pastguess
    guess_point = 0
    print("\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n")

    for i in pastguess:
        if guess == i:
            print("Letter already guessed.\n")
            print(code_target)
            return
        else:
            continue


    if guess.isalpha() == False or len(guess) != 1:
        if guess == word:
            print("\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n")
            print(f"WINNER!\n\nThe word was {word}.")
            lives = 0
            return
        elif len(guess) == len(word):
            lives -=1
            print("Incorrect guess, you lost 1 life.\n")
            print(code_target)
            return
        else:
            print("Please enter a single letter.\n")
            print(code_target)
            return

    pastguess += guess

    for i in word:
        x += 1
        if i == guess:
            temp_target += i
            point += 1
            guess_point += 1
        elif code_target[x] == "?":
            temp_target += "?"
        else:
            temp_target += i
    if guess_point != 0:
        print("Correct Guess!\n")
    else:
        lives -= 1
        if lives == 0:
            print(progress[lives])
            print(f"\nGame Over, you lose! The word was {word}.")
            return
        else:
            print(f"Incorrect Guess, you lost 1 life.\n")
    code_target = temp_target
    temp_target = ""
    if word == code_target:
        print("\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n\n")
        print(f"WINNER!\n\nThe word was {word}.")
        lives = 0
        return
    else:
        print(code_target)

while lives !=0:
    print(progress[lives])
    print(f"\nLetters already guessed: {pastguess}")
    print(f"Lives Remaining: {lives}")
    attempt(input("Player 2, guess a letter: ").lower(),-1)
input("")
