[[App Development]]
**Variable declaration

-   var (varname) = (value)
    

Printing variables

-   Put $ before variable
    

If statements

-   when (variable) {
    

-   (condition) -> (code)
    

Unchangeable array = listOf

Changeable array = arrayListOf

Dictionaries = mapOf(key to value)

.getOrDefault

-   If can’t get, creates default value
    

Changeable dictionary = hashMapOf

.put

-   Adds key value pair
    

  

# App Development

## Timber

-   Used for creating logs in logcat
    

-   Useful for debugging and making sure code runs properly
    

## Lifecycle

-   Allows a class to observe and react to the states of another class
    

To implement:

-   Extend the class with LifecycleObserver
    
-   Ask for args upon creation (lifecycle: Lifecycle)
    
-   Add observer to passed lifecycle in constructor (.addObserver(this))
    

## SavedInstanceState

-   The function onSavedInstanceState gets called after a program stops
    

-   Used to store different variables you want to keep into a bundle
    

ex) outState.putInt(intVariable)

  

-   onRestoreInstanceState retrieves the information you put into your variable
    

-   Furthermore, have code that imports savedInstanceState if the bundle isn’t null
    

## App Architecture

### UI Controller

-   Displaying data, capturing user events
    
-   Should have as little responsibility as possible
    
-   Handles navigation
    

### ViewModel

-   Abstract class that survives configuration changes
    

-   Holding data needed for the UI, and preparing it for display
    

-   No size restrictions :o
    

-   Has live data that it sends to ui controller
    
-   Should never reference fragments, activities, or views
    

#### Implementation

-   Initialize the viewmodel in the UI controller:
    

ex) private lateinit var viewModel: GameViewModel

-   Request viewmodel from ViewModelProviders.of(fragment).get(viewModel::class.java) and store it
    
-   Put this in onCreateView
    

#### Factories

-   Act as constructors for viewmodel
    

### LiveData

-   Observable data holder class that is lifecycle aware
    
-   UI controllers observe the live data
    
-   Will only update ui controllers that are on screen
    

#### Implementation

-   Turn variable into livedata
    

//in ui controller onCreate method

-   viewModel.score.observe(this, Observer { newScore ->
    

updateScoreText(newScore)

//Score changes

score.value = 1

#### Encapsulating Live Data

-   Create a variable for a mutable live data and then a livedata variable to get the mutable live data
    

## Databases

#### DAO

## Threading

-   Processors perform code, and the actions to run code are called threads
    
-   It’s important to not perform long-running operations on the UI thread to prevent blocking and crashing
    

### Coroutines

-   Handles long-running tasks efficiently
    
-   Can signal errors with exceptions
    
-   Do the same as callbacks but differ in code
    
-   Asynchronous
    

-   Runs independently from the main execution steps of program
    

-   Non-blocking
    

-   Doesn’t block main ur UI thread
    
-   Instead, it just suspends the thread and does other work until ready
    

Coroutines need…

-   Jobs
    

-   A background job that is cancellable 
    

-   Dispatcher
    

-   Sends coroutines to run on various threads
    

-   Scope
    

-   Combines information to define the context in which coroutines run
    

#### Implementation

-   Create a coroutine in the main thread that runs a suspend function
    
-   Use Dispatchers.IO to call the long-running work**