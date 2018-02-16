### Example of bad code:

```
 public List<int[]> getThem() {
   List<int[]> list1 = new ArrayList<int[]>();
   for (int[] x : theList)
    if (x[0] == 4)
      list1.add(x);
   return list1;
 }
```

The context in the above code is not implicit, it leaves us with the questions:

* What kinds of things are in theList?
* What is the significance of the zeroth subscript of an item in theList?
* What is the significance of the value 4?
* How would I use the list being returned?

### Good

```
 public List<int[]> getFlaggedCells() {
   List<int[]> flaggedCells = new ArrayList<int[]>();
   for (int[] cell : gameBoard)
    if (cell[STATUS_VALUE] == FLAGGED)
      flaggedCells.add(cell);
   return flaggedCells;
 }
```

* What kinds of things are in theList? its a game board
* What is the significance of the zeroth subscript of an item in theList? its the status
* What is the significance of the value 4? its flagged or not
* How would I use the list being returned? we return all the cells that are flagged

### Better

Hiding the magic numbers and revealing intentions

```
 public List<Cell> getFlaggedCells() {
   List<Cell> flaggedCells = new ArrayList<Cell>();
   for (Cell cell : gameBoard)
     if (cell.isFlagged())
       flaggedCells.add(cell);
   return flaggedCells;
 }
```

Instead of `int`s we now use `Cell`
