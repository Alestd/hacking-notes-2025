#### Description

Want to play a game? As you use more of the shell, you might be interested in how they work! Binary search is a classic algorithm used to quickly find an item in a sorted list. Can you find the flag? You'll have 1000 possibilities and only 10 guesses.Cyber security often has a huge amount of data to look through - from logs, vulnerability reports, and forensics. Practicing the fundamentals manually might help you in the future when you have to write your own tools!You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_atlas/20/challenge.zip)

Additional details will be available after launching your challenge instance.

#### Hints 
1.-Have you ever played hot or cold? Binary search is a bit like that.
2.You have a very limited number of guesses. Try larger jumps between numbers!
3.-The program will randomly choose a new number each time you connect. You can always try again, but you should start your binary search over from the beginning - try around 500. Can you think of why?

#### Hints 
The program will randomly choose a new number each time you connect. You can always try again, but you should start your binary search over from the beginning - try around 500. Can you think of why?
# Solución 

````
alestd-picoctf@webshell:~$ ssh -p 59035 ctf-player@atlas.picoctf.net
ctf-player@atlas.picoctf.net's password: 
Welcome to the Binary Search Game!
I'm thinking of a number between 1 and 1000.
Enter your guess: 720
Higher! Try again.
Enter your guess: 725
Higher! Try again.
Enter your guess: 728
Higher! Try again.
Enter your guess: 729
Higher! Try again.
Enter your guess: 730
Higher! Try again.
Enter your guess: 800
Higher! Try again.
Enter your guess: 900
Higher! Try again.
Enter your guess: 100
Higher! Try again.
Enter your guess: 1000
Lower! Try again.
Enter your guess: 960
Lower! Try again.
Sorry, you've exceeded the maximum number of guesses.
Connection to atlas.picoctf.net closed.
alestd-picoctf@webshell:~$ ssh -p 59035 ctf-player@atlas.picoctf.net
ctf-player@atlas.picoctf.net's password: 
Welcome to the Binary Search Game!
I'm thinking of a number between 1 and 1000.
Enter your guess: 1000
Lower! Try again.
Enter your guess: 800
Lower! Try again.
Enter your guess: 500
Lower! Try again.
Enter your guess: 400
Lower! Try again.
Enter your guess: 200
Higher! Try again.
Enter your guess: 300
Higher! Try again.
Enter your guess: 350
Higher! Try again.
Enter your guess: 360
Lower! Try again.
Enter your guess: 355
Lower! Try again.
Enter your guess: 354
Lower! Try again.
Sorry, you've exceeded the maximum number of guesses.
Connection to atlas.picoctf.net closed.
alestd-picoctf@webshell:~$ ssh -p 59035 ctf-player@atlas.picoctf.net

ctf-player@atlas.picoctf.net's password: 
Permission denied, please try again.
ctf-player@atlas.picoctf.net's password: 
Welcome to the Binary Search Game!
I'm thinking of a number between 1 and 1000.
Enter your guess: 500
Lower! Try again.
Enter your guess: 400
Lower! Try again.
Enter your guess: 300
Lower! Try again.
Enter your guess: 200
Lower! Try again.
Enter your guess: 100
Higher! Try again.
Enter your guess: 150
Lower! Try again.
Enter your guess: 180
Lower! Try again.
Enter your guess: 170
Lower! Try again.
Enter your guess: 154
Lower! Try again.
Enter your guess: 155
Lower! Try again.
Sorry, you've exceeded the maximum number of guesses.
Connection to atlas.picoctf.net closed.
alestd-picoctf@webshell:~$ ssh -p 59035 ctf-player@atlas.picoctf.net
ctf-player@atlas.picoctf.net's password: 
Welcome to the Binary Search Game!
I'm thinking of a number between 1 and 1000.
Enter your guess: 500
Lower! Try again.
Enter your guess: 250
Lower! Try again.
Enter your guess: 100
Lower! Try again.
Enter your guess: 50
Higher! Try again.
Enter your guess: 75
Higher! Try again.
Enter your guess: 65
Higher! Try again.
Enter your guess: 85
Higher! Try again.
Enter your guess: 90
Lower! Try again.
Enter your guess: 87
Congratulations! You guessed the correct number: 87
Here's your flag: picoCTF{g00d_gu355_bee04a2a}


```