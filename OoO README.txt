# ATotPD READ ME: Character sheet development order of operations to calculate JUST raw stats outputs and their inorganic level-up fabrications. thirteen (13) player-managed stats, 9 physical stats, 4 bonus augmentation stats, are raised by one point at a time, which raises the attribute outputs of each stat respectively.  


Vitality through Agility are physical stats which go up by 1 per point spent. leveling up adds the stored (spent) points to the output.  
so a creation sheet would have level 0 outputs:     

Vit: (8) 8.   
and a finished sheet would add the spent points (SP) to the output and look like:   

Vit (8) 16.     

every spent point to the (SP) raises both the sp and output by 1.   
after spending 13 stat points, and both values are raised, a level up bonus is awarded and all stats are raised by the number of (SP) spent points. 



from 0 to 1: 
vit: (8) 8 -to- (8) 16.  


from 1 to 2: (+4 to vit @ level 1) 
BEFORE: Vit: (12) 20  
AFTER: (level 2) Vit: (12) 22.  


one more time, from 2 to 3: (+5 to vit @ level 2)       

BEFORE: Vit: (17) 27  

AFTER: Vit: (17) 44.   



this is the manner by which the top 9 stats are calculated between levels. 

The bottom four stats, Luck, Willpower, Flexibility, and Rage have to compare to one another and perform a subtraction.  
Luck and Willpower negate each other, Rage and Flexibility negate each other. 

when calculating stats, they are compared to each other and the higher and lower are determined.  

the higher is reduced by the amount in the lower. 


so luck or willpwer. rage or flexibility. pick one, or face some pretty funny consequences.

 

the algorithm is as follows:    


Luck/Flexibility (16) 72 | Willpower/Rage (1) 15      


leveling up and +3 points  

BEFORE: luck/flex: (19) 75 | Will/rage: (1) 15  
AFTER: L/F: (19) 59 | W/R: (1) 16...    

since that's a bad prefab and could no way correspond to the (SP) to output ratio, the number went down after leveling up even though 3 points were spent on it.
   
let's spend 13 on it, even though it's an invalid move...


BEFORE: L/F: (32) 72 | W/R: (1) 17   
AFTER: L/F: (32) 87 | W/R: (1) 16... 


if the output of the lower stat is higher than the spent points of the preferred stat, it will eventually drop below the lower stat's output because that number doesnt go down until the other number is lower.  There's a natural penalty for not adhering strictly to the stat of choice and maintaining a higher (SP) to output ratio on the favorable bonus stat.   
after leveling up is finished, comparing the 13 stats and calculating outputs is next. 
this begins with your 4 bonus stats. 


Luck is calculated by its output divided by your level times 5 plus 1k and then plus 1: 
(Luck/((Lv*40(+10000))+1) 


a similar process is used on the remaining 3: 


(Will/((Lv*10)+2500))+1) for will

(Flex/((Lv*20)+5000))+1)

and (Rage/((Lv*5)+1250))+1)   



it clearly takes huge outputs to make these worthwhile but an example of how flexibility works is it is multiplied to all your stat outputs other than vitality.  
a Flex of 1650 at level 30 is an output of 1.279661016949153    

these outputs are rounded up from 6 (not 5) and cut off after the 4'th decimal after comparing the fifth: 1.2796(6); 1.2797; 1.28; ~ 1.3   



1.3% bonus multiplier for flex is applied to intelligence, wit, dexterity, defense, stamina, strength, speed, and agility.  
take an output of 84, for example, and multiply it by 1.3: 109.2 ~ 109, since outputs dont use decimals, always round down below 0.6.  


Rage, Willpower, and luck are augments in a similar fashion but arent applied to all the stats.  
so after raising the initial output by the flex % bonus, calculating the "alternative outputs" for rage and willpower augments is prudent. luckily they dont apply to as many stats.  
willpower does not apply to Vit, Int, and Wit, and Rage only applies to Stm, Str, Spd, and Agi (dat berserker's loss of dexterity! :O).  


once you've calculated your stat points, compensated your augmentation stat outputs, compiled their percentile bonuses, applied flex to all stats (except vitality!), and calculated the reserve augmentations for rage and will, you're ready to calculate spirit! (now it gets a little more straight forward)


7. Spirit: (sum total of all acquired stat points)+(Will-Rage[permitting negative values])

8. Wisdom: (Int*Wit)/(Level*10)+([Int]+[Wit])  {[denotes stat point expenditures not outputs]}

9. Perception: ((Int+Wit+Wisdom)/3)*Luck%

10. Appearance: ((Vit+Int+Dex+Stm+Str)/5)+Spirit

11. Charisma: ((Int+Wit)*(Spd+Agi)+Appearance)/wisdom

12. Endurance: ((Vit+Dex+Stm+Agi)/4)*Flex%

13. Barter: (Appearance+Charisma+((Int+Wit+Def+Agi)/4))*Luck%

14. Accuracy: ((Perception+Int+Dex+Agi)/4)*Luck%

15. Evasion: ((Perception+Wit+Spd)/3)*Flex%

16. Stealth: (Dex+Evasion)*((Wit+Stm+Agi)/3))/((End+Appearance+Perception)/3)*Flex%

17. Hit Points: (((Vit*1000)*Flx%)+((End+Agi)*Def))+(str^2) = HP total | HP total*Flex% = HP OUTPUT

18. HP regeneration rate: (HP total*(Endurance+Agi))/((HP OUTPUT+((Endurance+Agi)*Def)=HP per hour)/60=HP per min (divide by 60 for per second)

19. PhA: (Str*Spd)*Flex%

20. PhD: (Def*Stm)*Flex%

21. Mana: (Spirit+Charisma)-(Rage^2)

22. Mana regeneration rate: (((Wisdom+Int+Wit)/3)= mana per hour)/60= mana per minute (divide by 60 for per second)
23. MgA: ((Wit*Dex)*Flex%)*Will%
24. MgD: ((Vit*Int)*Flex%)*Will%
(how do i get word wrap turned on ffs?)
