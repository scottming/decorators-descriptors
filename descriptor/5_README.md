basically by build the object that descriptors the class and that as a parameter to this function and this function can do whatever it likes to that object and return a class.

so, it's the same idea of the function decorator applied to a class now.

Usaually what happens is that is not that a whole new class is created but it's more common that th class itself is returns after being manipulated in some way.

and this is the manipulation that's going on first of all take a look at the what happened to the descriptor it's much simpler now because it doesn't need the field count anymore it just has this `__set__`, this `__set__` assumes that there is a storage name attributes in the descriptor but they don't know in it that creates it and there is no need for the `__get__` anymore because the storage group will be the public name of that property, and the whole magic happens in this code is not very diffcult to understand, so the decorator gets the class as an argument and then it iterates over the items in the class dictionary.

The class dictionary is where the class attributes are stored how many are in this  class dictionary for this item which is an instance of long length this other item which is an instance of may this item which is a function and this other item  which is a function so you have four objects, so this look goes around four times and each time it checks whether the attribute that I'm looking at is an instance of nonblank, if it is a instance of non  blank because now I'm looking at the dictionary of this class  I have the name which is this name .

when this class is defined the class decorator really doesn't change anything in the class but it goes into the different descriptors that are used in the class configures them correctly.