 README: Sentence Analysis Algorithm
🔍 Purpose
This algorithm processes a user-inputted sentence to compute:

Total number of characters (excluding spaces and punctuation).

Total number of words.

Total number of vowels (a, e, i, o, u).

🧮 VARIABLES USED
Variable	Type	Description
character_count	INTEGER	Counts all non-space characters.
word_count	INTEGER	Counts the number of words.
vowel_count	INTEGER	Counts the number of vowels in the sentence.
vowel	STRING	A string containing all vowels "aeiou"
sentence	STRING	Input sentence provided by the user.

🧾 STEPS
1. Initialize variables
Set all counters (character_count, word_count, vowel_count) to 0.

2. Read user input
Prompt the user to enter a sentence and store it in the variable sentence.

pseudocode
Copy
Edit
Read(sentence)
3. Iterate through the sentence
Loop through each character in the sentence using a for loop.

pseudocode
Copy
Edit
for i FROM 0 TO sentence.length - 1 DO
4. Character and word counting
Check each character to determine whether it's:

A space " " → This typically indicates a new word.

A period "." → Treat as the end of a sentence and thus a new word.

Any other character → Counted as part of a word (i.e., a character).

pseudocode
Copy
Edit
IF sentence[i] == " " THEN
    word_count := word_count + 1
ELSE IF sentence[i] == "." THEN
    word_count := word_count + 1
ELSE
    character_count := character_count + 1
END IF
✅ Note: The condition sentence[i] === "" should likely be sentence[i] == " " (space character).

5. Vowel counting
For each character, check if it is in the vowel string:

pseudocode
Copy
Edit
IF vowel.includes(sentence[i]) THEN
    vowel_count := vowel_count + 1
END IF
✅ Final Output
After the loop ends, output the final counts:

Total characters

Total words

Total vowels

