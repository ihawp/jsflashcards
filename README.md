# JS Flashcard App

Should be scalable

Should look good

Should be simple

Should be able to have other sets (maybe not just JS flashcards)

Should be able to search for sets

Should be able to create set (as user)

Should be able to skip flashcard

Home page should show most popular sets?

Should track data related to users 'used' sets:
- if they don't complete the set will say 50% completed (or whatever %)
- correct or wrong scale (when flipped user presses a button to tell the computer what really happened in their head)
  - could show with like amount of times wrong/right (and have that be a value that is just incremented)

Tech?
- MySQL database
- React (tsx)
- Tailwind or CSS?
- Express or Node?

Pages
- home (will display sets and search bar to look for specific sets) (can click on set to preview (click begin and you will be taken to flashcard page))
- account (for delete and whatever)
- privacy policy (not sure if technically required if I host on (name).ihawp.com as ihawp.com has public privacy policy, will look into that)
- flashcard(s) (displays flashcards one at a time, once you flip the card you are asked if you got it wrong or right...! once you press next question is displayed!)

Database Structure?
Where to store salt?
- accounts (no need for profile or stuff like that)
  - id (auto increm, primary)
  - email (tinytext)
  - password (varbinary)
  - acc_creation (timestamp)
  - login (timestamp)
  - logged_in (bool)
  
- sets
  - id
  - title
  - description
  - updated (timestamp)
  - ? questions (JSON) ? but if not (ref to flashcards below) (max-text length 255, max questions (per set) 50 or something like that would make it fine)

- flashcards
  - id
  - set_id
  - question
  - answer
