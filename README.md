# MDP REPRESENTATION

## AIM:
To represent a Markov Decision Process(MDP) problem in the following ways.

1.Text representation

2.Graphical representation

3.Python - Dictonary representation

## PROBLEM STATEMENT:

### Problem Description
An elevator in a 3-floor building must decide whether to move up, down, or stay idle to serve passengers efficiently.

### State Space
S = {Floor 1, Floor 2, Floor 3}


### Sample State
Floor 2
### Action Space
1.Move Up

2.Move Down

3.Stay
### Sample Action
Move Up

### Reward Function
+10 if serving a waiting passenger.

–2 if moving without serving.

0 if idle.

### Graphical Representation
<img width="782" height="531" alt="image" src="https://github.com/user-attachments/assets/d62b4d94-7722-41cc-88e8-69a299335b32" />

## PYTHON REPRESENTATION:
```
P = {
    1: {   # Floor 1
        0: [(0.8, 2, +5, False), (0.2, 1, -1, False)],
        1: [(1.0, 1, 0, False)],
        2: [(1.0, 1, 0, False)]
    },
    2: {   # Floor 2
        0: [(0.8, 3, +10, False), (0.2, 2, -1, False)],
        1: [(0.8, 1, +5, False), (0.2, 2, -1, False)],
        2: [(1.0, 2, 0, False)]
    },
    3: {   # Floor 3
        0: [(1.0, 3, 0, False)],
        1: [(0.8, 2, +5, False), (0.2, 3, -1, False)],
        2: [(1.0, 3, 0, False)]
    }
}
```

## OUTPUT:
```
>>> P[1]
{
 0: [(0.8, 2, 5, False), (0.2, 1, -1, False)],
 1: [(1.0, 1, 0, False)],
 2: [(1.0, 1, 0, False)]
}

>>> P[2]
{
 0: [(0.8, 3, 10, False), (0.2, 2, -1, False)],
 1: [(0.8, 1, 5, False), (0.2, 2, -1, False)],
 2: [(1.0, 2, 0, False)]
}

>>> P[3]
{
 0: [(1.0, 3, 0, False)],
 1: [(0.8, 2, 5, False), (0.2, 3, -1, False)],
 2: [(1.0, 3, 0, False)]
}
```
## RESULT:
The Elevator Control MDP was successfully represented. The agent makes optimal moves to minimize passenger wait time
