# bag-o-loot
Working with command line parameters

Bag o' Loot

This exercises will help with your comprehension of command line parameters.

Setup

mkdir -p ~/workspace/python/exercises/cli && cd $_
touch lootbag.py
Instructions

You have an acquaintance whose job is to, once a year, delivery presents to the best kids around the world. They have a problem, though. There are so many good boys and girls in the world now, that their old paper accounting systems just don't cut it anymore. They want you to write a program that will let them do the following tasks.

Add a toy to the bag o' loot, and label it with the child's name who will receive it. The first argument must be the word add. The second argument is the gift to be delivered. The third argument is the name of the child.

python lootbag.py add kite suzy
python lootbag.py add baseball michael
Remove a toy from the bag o' loot in case a child's status changes before delivery starts.

python lootbag.py remove suzy kite
python lootbag.py remove michael baseball
Produce a list of children currently receiving presents.

python lootbag.py ls
List toys in the bag o' loot for a specific child.

python lootbag.py ls suzy
Specify when a child's toys have been delivered.

python lootbag.py delivered suzy
Requirements

Write a test before you write implementation code

# This is only an example. If I find this code in your project
#  I will make you go back and delete it and write your own test.
def test_toys_for_child_can_be_added_to_bag ()
{
    lootBag = Bag()
    lootBag.add_toy_for_child("kite", "suzy");
    self.assertEqual("kite", lootBag.child_items("suzy")[0]);
}
Items can be added to bag, and assigned to a child.
Items can be removed from bag, per child. Removing ball from the bag should not be allowed. A child's name must be specified.
Must be able to list all children who are getting a toy.
Must be able to list all toys for a given child's name.
Must be able to set the delivered property of a child, which defaults to false to true.
Bonus Features

Write a response for the argument python lootbag.py help that lists all of the possible arguments, and what they do.
Create a shortcut combination of arguments that can remove all toys from the bag for a child who has been deemed naughty.
Persistent Storage

You must persist the data to disk, so that you can use it between executions of the application. You will need to write the data into text files. As for how you store it, create a quick ERD that represents the two types of data in this application.

How are they related to each other?

How can you store that relationship when you are writing the data to disk?

Pro tip: The uuid module in Python can generate universally unique identifiers for each set of data that you need to store. For example, there will be children with the same name, so you will need a truly unique identifier for each one.
child_id

child_name

a8098c1a-f86e-11da-bd1a-00112444be1e	Victor Hoebling
6fa459ea-ee8a-3ca4-894e-db77e160355e	Franz Ferdinand
