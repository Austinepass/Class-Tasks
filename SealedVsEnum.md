**Enum Class**

An enum class is a special class used to represent a set of constant values, for example, we can represent 
the set of numbers in a fair die {one, two, three, four, five, six} with an enum class. These enum constants can also be initialized.
```
enum class Die(val num: Int) {

    //Each constant is an instance of the enum class Die(Int) that takes in an integer value
    ONE(1), 
    TWO(2), 
    THREE(3), 
    FOUR(4), 
    FIVE(5), 
    SIX(6)
}
```
  
  **Sealed Class**
  
 A sealed class just like the enum class is used to group a set of values, the distinction is in the fact that with enum classes, only a single
 instance of the constants exists (e.g you can't have more than a single value of 'two' in a fair die, whereas within a
 sealed class, multiple instances can exist.
 
``` 
 sealed class Card {
    class Red() : Card()
    class Yellow() : Card()
    
     fun referee(card: Card)
      {
        val text = when(card) 
        {
          is Red -> "Red card"
          is Yellow ->  "Yellow card"
        }
      
        print(text)
      }

}
```
