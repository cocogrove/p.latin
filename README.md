p.latin
=======

# variable and value set to make trasnalting simple
pyg = 'ay'

# list of variables and values to refer back to while coding

# ask user to insert word
original = raw_input('Enter a word:')

# keeps the letters of said word lower case
word = original.lower()

# takes the first letter of 'original' which is the user's word
first = original[0]

# list of vowels to refer back to in order to keep the code cleaner (otherways of executing this step)
vowel = ["a", "e", "i", "o", "u"]

# set a new variable which is user's word + 'ay'
new_word = word + pyg

# this 'if' checks that the word contains letters (>0) and that the word only contains alphabetical letters and not numbers / signs
if len(original) > 0 and original.isalpha():
    # this nested 'if' checks that the first letter (previous variable) is not included in the vowels (also previous variable)
    if first in vowel:
        # if so, the computer will print the user's word + 'ay'
        print str(new_word)
    else:
        # if not, it will take the first letter (consonant), move it to the back of the word, and then add 'ay'
        new_word = word[1:] + first + pyg
        # then it will print the final product to the screen
        print new_word
else:
    # if the word failed the earlier criteria (>0) (isalpha()) then prints "empty"
    print 'empty'
