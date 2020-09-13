The following code is a simulation of a dice. It uses the Random Library.

```.py
#3- Repeat process 1000 times and record the counts for each face
import random
counts = [0, 0, 0, 0, 0, 0]
num_trial = 20000
for trial in range(num_trial):
    number = random.randint(0,60)
    if number < 10:
        counts[0] += 1
    elif 9 < number < 20:
        counts[1] += 1
    elif 19 < number < 30:
        counts[2] += 1
    elif 29 < number < 40:
        counts[3] += 1
    elif 39 < number < 50:
        counts[4] += 1
    elif 49 < number < 60:
        counts[5] += 1
for index, c in enumerate(counts):
    error = c - num_trial/6
    print("Number of {}s: {}, expected {}, error {}".format(index+1,c, num_trial/6, error))


```
