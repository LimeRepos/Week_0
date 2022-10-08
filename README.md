# Week 0

## Task

Using Remix develop a contract for a book library.

1. The administrator (owner) of the library should be able to add new books and the number of copies in the library.
2. Users should be able to see the available books and borrow them by their id.
3. Users should be able to return books.
4. A user should not borrow more than one copy of a book at a time. The users should not be able to borrow a book more times than the copies in the libraries unless copy is returned.
5. Everyone should be able to see the addresses of all people that have ever borrowed a given book.


## Solution description

The contract `Library.sol` has all the funcionallity specified above. 

Number one was solved by using the onlyOwner modifier in the `Ownable.sol` contract. I decided to add an extra function that lets the admin add more copies of a book. The implemented functions where `addNewBook` and `addCopies`.

For number 2 I supposed that "by their id" spec ment that the consults where made with the book id as a parameter. The implemented functions for this where `getName`, `isAvailable`, `availableUnits` and `borrowBook`

In number 3 I just implemented the funcion `returnBook(uint256 _id)`

Number 4 was solved by adding requires in most functions and managing well the mappings and arrays used.

Lastly, 5 is done by calling `viewBookBorrowers`

The code is decently documented. 
