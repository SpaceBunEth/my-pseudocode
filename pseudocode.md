# Cooking Your Favorite Meal: [Chef John's Tomato Sauce](https://www.allrecipes.com/recipe/235565/chef-johns-tomato-sauce/)
- - -
## Prerequisites:
- - - 

### A List of prerequisites for running Chief John's Tomato Sauce recipe.
- Chef (you or someone else) *preferably human*
- Clean Environment
- Source of heat - Ex: (Stove)
- Work surface - Ex: (Cutting Board)
- Cutting Tool - Ex: (Knife)
- Stirring Tool - Ex: (Wooden Spoon) Note: this will not work with a regular spoon.
- One Large Pot or Cauldron
- One Large Bowl
- Groceries/ Raw Food Items
    
    - Olive Oil - (<sup>1</sup>/<sub>4</sub>  Cup)
    - Onion - (x1)
    - Rib Celery - (x1)
    - Salt - (1 <sup>1</sup>/<sub>4</sub> teaspoon)
    - Garlic - (4 cloves)
    - San Marzano Tomatoes - (2 Cans/ 28 ounces)
    - White Sugar - (2 teaspoons)
    - Anchovy Paste - (1 teaspoon)
    - White Wine Vinegar - (1 teaspoon)
    - Dried Italian Herbs - (<sup>1</sup>/<sub>2</sub> teaspoon)
    - Red Pepper Flakes - (<sup>1</sup>/<sub>4</sub> teaspoon)
    - Tomato Paste - (1 tablespoon)
    - Italian FlatLeaf Parsley - (2 tablespoons)
    - Water - (As needed - 1 Cup)
- - - 
## About:
- - -

Today We'll be cooking [Chef John's Tomato Sauce](https://www.allrecipes.com/recipe/235565/chef-johns-tomato-sauce/). This is a basic general purpose tomato sauce good for any appilcation requiring a tomato sauce base. Perfect for meat sauces or to top chicken parm!
### Creating a Sauce takes
- Time
- Heat
- Tools
- Fresh ingredients
- Preparation
- Senses (Taste, Sound, Apperance/ Sight, and Smell)

### The Tomato Sauce Should
Use all ingredients, be edible, serve about eight people, and take roughly 2 hours to complete.
- - - 
## INIT(): Variables
- - -
### 1. Chef
    The "Chef" is the most important element in this program. Without the Chef nothing will get done! Their special abilities are.

__Chef's Abilities__
- Return Environment Status - *Sense Environment*
- Control heatSource
- Control tools
- Manage ingredients
- Tells time
___
__PROPERTIES__
- .environment
    - .sight
    - .sound
    - .smell
    - .taste
- .heatSource
- .tools
- .ingredients
- .time

```Ex: Print (Chef.environment)```
"Will print out what the chef Tastes, Hears, Sees, and Smells"<br />
```Ex: Chef.heatSource(heatSource(value))``` "Sets heatSource temperature with chef"<br>
```Ex: Chef.tool(tools.woodenSpoon)``` "Selects the tool Chef equips"<br>
```Ex: Chef.ingredients(ingredients(Food, Amount))``` "Equips amount of specifed food item"
```Ex: Chef.time``` "Reads Time"
___
    
### 2. cleanEnvironment
    "cleanEnvironment" Shows only two types of data. True or False and can be defined as a Boolean. 
- True or False
___
__PROPERTIES__
- True
- False
___
### 3. heatSource
    "heatSource" controls the temperature through a flexable range of values. Starting from Low, mid-low, mid, mid-high, to high heat and change value at anytime if directed by "Chef".
___
__PROPERTIES__ 
- low 
- mid-low 
- mid 
- mid-high 
- high.

```Ex: heatSource(mid-low)```
___
### 4. tools
    "tools" refers to a list of objects needed to complete this task and can be accessed by "Chef"

### List of tools
- cuttingBoard
- knife
- woodenSpoon
- largePot 
- largeBowl
___

__PROPERTIES__

- tools.name

```Ex: Chef.tools(tools.cuttingBoard)``` "Chef Equips cuttingBoard"

___
### 5. ingredients
    "ingredients" is a 2 part List of ingredients and measurements that will be used to create the tomato sauce. Information of "How Much" there is of a particular ingrendient is also noted. 

### Ordered-List 
1. Olive Oil - (<sup>1</sup>/<sub>4</sub>  Cup)
2. Onion - (x1)
3. Rib Celery - (x1)
4. Salt - (1 <sup>1</sup>/<sub>4</sub> teaspoon)
5. Garlic - (4 cloves)
6. San Marzano Tomatoes - (2 Cans/ 28 ounces)
7. White Sugar - (2 teaspoons)
8. Anchovy Paste - (1 teaspoon)
9. White Wine Vinegar - (1 teaspoon)
10. Dried Italian Herbs - (<sup>1</sup>/<sub>2</sub> teaspoon)
11. Red Pepper Flakes - (<sup>1</sup>/<sub>4</sub> teaspoon)
12. Tomato Paste - (1 tablespoon)
13. Italian FlatLeaf Parsley - (2 tablespoons)
14. Water - (As needed - 1 Cup)

___
__PROPERTIES__

```
    ingredients {

            Food: [Olive Oil, Onion, Rib Celery, Salt, Garlic, San Marzano Tomatoes, White Sugar, Anchovy Paste, White Wine Vinegar, Dried Italian Herbs, Red Pepper Flakes, Tomato Paste, Italian FlatLeaf Parsley, Water]

            Amount: [0.25 Cup, 1, 1, 1.25 tsp, 4 clv, 28 ounces, 2 tsp, 1 tsp, 1 tsp, 0.5 tsp, 0.25 tsp, 1 tbsp, 2 tbsp, 1 Cup]

    }

```
```Ex: Chef.ingredients(ingredients(Food, Amount))``` "Equips amount of specifed food item"
___
### 6. time()
- - - 
    "time()" Can take a value. When "Chef" reads a "time(value)", "Chef" will pause for that predetermined period of time.
### time()
Wait for a curtain amount of time.
____
__PROPERTIES__

```Ex: time(1)``` "Wait for One Minute"
____
## Functionality:
- - -
### Prep Environment
```
    Function checkEnvironment
        IF cleanEnvironment === True
            PROCEED
        IF cleanEnvironment === False
            STOP

    Function checkGroceries
        Do I have these items in this amount?
        Compare List to items and quantities.
        IF True 
            PROCEED
        ELSE
            STOP

    Function setupHeatSource
        Chef.tool(tools.largePot)
        Chef.heatSource(heatSource(mid-low))


    Function Chop(x,y) // Pass ingredients to chop
        Chef.tool(tools.cuttingBoard)
        Chef.tool(tools.Knife)
        Chef.ingredients(ingredients.(x,y))
        ACTION CHOP // Chops up food
    
    Function Crush(x,y) // Pass ingredients to Crush
        Chef.tool(tools.woodenSpoon)
        Chef.tool(tools.largeBowl)
        Chef.ingredients(ingredients.(x,y))
        ACTION CRUSH // Crushes Up food

    Function WaitAndStir
        time(5)
        Chef.tool(tool.woodenSpoon)
        ACTION Stir
        Print (Chef.environment) 

    Function WaterAndStir
        time(15)
        Chef.tool(tools.woodenSpoon)
        Action Stir
            IF Chef.environment.sight === 'Water Level Low largePot'
                ACTION ADD ingredient(Food:[Water], .25)
        REPEAT x6
```

### Start Cooking
```
    Function Step1
        Chop(ingredients(Onion, 1))
        Chop(ingredients(Rib Celery, 1))
        ACTION ADD TO "largePot"
        setupHeatSource
        ACTION ADD ingredients(salt, 0.25)
            IF NOT Chef.environment.taste === "onions are very soft"
                WaitAndStir
                REPEAT
        Chop(ingredients(Garlic, 4))
        ACTION ADD TO "largePot"
        time(1)
        Print (Chef.environment)
        
    Function Step2
        Crush(ingredients(San Marzano Tomatoes, 28))
        
    Function Step3
        ACTION ADD TO "largePot" ingredients
        (Food: [White Sugar, salt, anchovy paste, white wine vinegar, Italian herbs, red pepper flakes], Amount: [ALL])
        
        Chef.heatSource(heatSource(mid))
            
            IF NOT Chef.environment.sight === 'Dry largePot'
                WaitAndStir
                REPEAT

        ACTION ADD ingredients(Food: [Tomatoe Paste], Amount: [ALL])
            IF NOT Chef.environment.sight === 'simmer largePot'
                WaitAndStir
                REPEAT

        ACTION ADD ingredients(Food: [San Marzano Tomatoes], Amount:[28])
        ACTION ADD ingredients(Food: [Italian FlatLeaf Parsley], Amount:[2])
            IF NOT Chef.environment.sight === 'simmer largePot'
                WaitAndStir
                REPEAT            
            ELSE 
                Chef.heatSource(heatSource(low))
        WaterAndStir
            
    Function Step4 
        Chef.environment.taste = "ALL DONE ENJOY!"
```
- - -
## Run Program:
- - -
```
checkEnvironment
checkGroceries
Step1
Step2
Step3
Step4
```
- - -
###### RETURN([Sauce](https://www.youtube.com/watch?v=HP9doLye26I))



