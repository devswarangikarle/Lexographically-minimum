# Lexographically-minimum
Tia has a three- letter word composed of lowercase letters from the English alphabet. Each letter in this alphabet is numbered from 1 to 26, with "a" being 1 and "z" being 26.  She created a numerical representation of this word by summing the values of its letters. For example, the word "cat" is represented as 3+1+20=24,

def find_lexicographically_minimum(n):
    for i in range(1, 27):
        for j in range(1, 27):
            for k in range(1, 27):
                if i + j + k == n:
                    return chr(i + ord('a') - 1) + chr(j + ord('a') - 1) + chr(k + ord('a') - 1)


n = int(input().strip())

result = find_lexicographically_minimum(n)
print(result)
