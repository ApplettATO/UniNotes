**Exam Prac**
Question 1:
T1 commit comes after T2 

Question 4: 2PL
what ever read lock can do write lock can also do

Transaction T1:
	Does not follow T1 as write-lock is placed on X after Y is unlocked

Transaction T2:
Follows 2PL

Transaction T3:
	Does not follow as write-lock on Y is downgraded to a read-lock before a write-lock is placed on X

**Tutorial 12**
Question 1:

T2 Start | *Checkpoint* | T1 Start | T1 Commit | T3 Commit | *Crash* | 

Part A
- Redo. T1 was committed before system crash, some updates may not have been flushed to disk yet (Due to No-Force), need to redo to guarantee atomicity and durability
Part B
- Undo needed to guarantee atomicity, after undo T2 is restarted
Part C
- No Action as updates of T3 have been flushed to disk at checkpoint

Question 2:
undo T8
redo T6
undo and restart T9

Question 5: RECOMMEND A QUESTION THAT MIGHT 