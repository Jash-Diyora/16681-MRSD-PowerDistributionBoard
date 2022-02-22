# 16681: MRSD Project / Programming Familiarization - 1
## Jashkumar Diyora (jdiyora)
### README Questions

Note: Medium mode is set using startup.cpp

Q1. Write an overview of how your AI works, including how it detects where projectiles will fall and how it chooses where to go.  
Solution: A boolean vector `safeSpots` of size width+1 is constructed for each player at each time step, which is meant for recording which discretized position is safe and which is unsafe. I determine the values in it by considering the current explorations & projectiles. For explorations, as long as there is an exploration, I mark positions within the exploration range as unsafe. As for projectiles, after predicting when it will fall and where it would fall with basic physics knowledge, I mark the 2 positions at the left and the right of predicted falling point as unsafe if it will fall in the next 50 timesteps. This way, my AI would have enough time to escape from incoming missiles.


Q2. What challenges did you face when writing an AI?  
Solution: First part is understanding the physics behind it, some small cout statements could save big time as in to know that gravity is -9.81 and not 9.8, the center is 100, left is 0-100 and right is 100-200. Values greater than 200 and less than 0 were not much issue since it wont land on the spot we need to worry about. 


Q3. How well does your AI work on a Hard scenario? If it doesn’t work, why? If it does, try harder scenarios and see when it does fail and explain why?  
Solution: Lets talk about each levels:
1. Easy/Medium: Very similar behaviour in both levels since player speed variable is same with minor difference in enemy construct.
2. Hard: It was able to dodge it for a while but after a point it dies and may be major factor could be change explosion time with doubled launchers but still a bit satisfactory results.
3. Very hard/Impossible: I'd like to name this levels as instant death since defence barely worked out for 2 seconds.  
 
Q4. What did you think of the assignment and did it meet its goals? Why or why not?  
Solution: Although I had background in cpp but no doubt it is one of the most skill exhaustive coding assignment I have seen recently, I struggled a bit initially to acquire all the new cpp concepts since used in this project but it also gaved me a good idea of cpp file management system, and I even learnt about cmake and make.
