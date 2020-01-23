# Santa's Workshop Tour 2019
https://www.kaggle.com/c/santa-workshop-tour-2019/overview/description

This competition proposed a mathematical optimization problem where we should minimize the following function:

![equation](https://latex.codecogs.com/gif.latex?score%20%3D%20preference%20%5C%3A%20cost%20&plus;%20accounting%5C%3A%20penalty)

where

![equation](https://latex.codecogs.com/gif.latex?accounting%5C%3A%20penalty%20%3D%20%5Csum_%7Bd%3D100%7D%5E%7B1%7D%20%5Cfrac%7B%28N_%7Bd%7D%20-%20125%29%7D%7B400%7D%20%7BN_d%7D%5E%7B%28%20%5Cfrac%7B1%7D%7B2%7D%20&plus;%20%5Cfrac%7B%5Clvert%20N_d%20-%20N_%7Bd&plus;1%7D%20%5Crvert%20%7D%7B50%7D%20%29%7D)

```
These sum up per family, and the total represents the preferencecost.

    choice_0: no consolation gifts
    choice_1: one $50 gift card to Santa's Gift Shop
    choice_2: one $50 gift card, and 25% off Santa's Buffet (value $9) for each family member
    choice_3: one $100 gift card, and 25% off Santa's Buffet (value $9) for each family member
    choice_4: one $200 gift card, and 25% off Santa's Buffet (value $9) for each family member
    choice_5: one $200 gift card, and 50% off Santa's Buffet (value $18) for each family member
    choice_6: one $300 gift card, and 50% off Santa's Buffet (value $18) for each family member
    choice_7: one $300 gift card, and free Santa's Buffet (value $36) for each family member
    choice_8: one $400 gift card, and free Santa's Buffet (value $36) for each family member
    choice_9: one $500 gift card, and free Santa's Buffet (value $36) for each family member, and 50% off North Pole Helicopter Ride tickets (value $199) for each family member
    otherwise: one $500 gift card, and free Santa's Buffet (value $36) for each family member, and free North Pole Helicopter Ride tickets (value $398) for each family member
    
```
The secret to solving it was to linearize the problem and use mixed integer programming.

I would like to thank **Heng CherKen** for your great ideas here: https://www.kaggle.com/c/santa-workshop-tour-2019/discussion/120764

My implementation was developed using Gurobi with academic license.
