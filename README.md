# TerminalDungeonQuest
This s a text-based dungeon crawler game implemented in C#. Players can choose from various character classes such as Warrior, Mage, and Rogue, each with unique abilities and attributes. 

Steps is completed when you create a PR too the master branch with the changes and adding me as the aprover, Call the PR Step# and a short but informative description of the changes that is in this PR
we will do **Squash Commits** so dont worry about informative local commit messages so commit often, happy about anychange you commit it localy, and then you push it to server to youown branchnow the PR text will be the commit message on master.
i want only 1 PR per step, so do all work and commit often the 

eksempel på kossen PR text skal se ut når dette er gjort 
"Step 55: Addet combat logic for elite enemyes"

Step 1:
 - [x] Do a git pull on this repo (ikke fork, bare vanilla clone) etter på cd inn i folder 
 - [x] Create a new branch form master and add a SLN named TerminalDungeonQuest.sln inside your 
 - [x] Create a new console project inside the new folder, call the projety call this project DungeonGameSimulator
 - [x] Create a new classlib project inside the new folder, call the projety call this project DungeonGameLogic
 - [x] Create a referance to the classlib DungeonGameLogic inside the DungeonGameSimulator 

Step 2:
 - [x] Create a new class in the DungeonGameLogic project named Character.
 - [x] Add common properties that all characters (like Warrior, Mage, Rogue) might share.
       Such as Name, Health, Strength, Energy, Mana, Gender(male, female), Speed, Agilty, Thac0 (https://dungeonsdragons.fandom.com/wiki/THAC0)
 - [x] Add common function that all charcther have, like attack, walk, sleep, jump, just add them like
     `public void NameOfCommonFunction (int defaultInput)
     {
          throw new NotImplementedException();
     }` 
     for now but one for each common functinality must be added
 - [x] Create derived classes for each character type (Warrior, Mage, Rogue) in the DungeonGameLogic project. Ensure these classes inherit from the Character base class.
 - [x] Each class should override or extend the base class with specific properties or methods relevant to that character type (e.g., CastSpell() for Mage, becaus this is not a common so mage class needs its owne CastSpell and such)
 - [x] Create an Enemy class with properties like Type, Health, and Damage.
 - [x] In DungeonGameLogic, create a class named GameEngine.
 - [x] Implement initial methods such as StartGame(), CreateCharacter(), and CreateEnemy()
 - [x] In DungeonGameSimulator, write code in Main() to start the game, create a character, and create a enemy.

Step 3:
 - [x] Every class will need a AC (Armour class) 
 - [x] Create a red team (band of 4 enemyes, the enemyes shold be 1 hunter, 1 mage, 1 Paladin and 1 warrior)
 - [x] Create a blue team (band 4 Friendlyes with the same setup 1 hunter, 1 mage, 1 Paladin and 1 warrior)
 - [x] Simulate 100 battles between red and blue, dump alle action stats and full battel log in json format and add to PR when checkin.
 - [x] To check if hit use ----> (THAC0 − Target AC = Required Roll)
 - [x] ROLLS are a D20 so create a Random that gives between a inn 1-20...
 - [x] use the Speed atribute to calculate who attacks first for each step,,, each team take on turn each, so 1 attack then other team attacks and so on
 - [x] The attacker should chose a random target for now
 - [x] Log all actions, outcomes, and stats for each battle.
 - [x] Format the entire battle log in JSON for easy analysis and debugging. This log should capture detailed sequences of moves, hits, misses, and outcomes of each battle.
 - [x] Once implemented, all changes should be committed to your branch. Ensure the pull request includes A full battle log in JSON format.
 

#Note: the Battle sim is just a for loop 0-99
Each team figths til all memnber of opposing team has 0 in healt... 


#Note: StartGAme(); should start with somthing like this 
Console.WriteLine("Welcome to Terminal Dungeon Quest!");
Console.WriteLine("Please choose your character class:");
