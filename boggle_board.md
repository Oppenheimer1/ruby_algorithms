# Boggle Board
#### This function taks a string and converts it so that all the words are converted to lowercase words and are joined by dashes.
```
class BoggleBoard
  
    def initialize (board)   
      @board=board
    end
    
    def create_word(board, *coords)
      coords.map { |coord| @board[coord.first][coord.last]}.join("")
    end

    def get_col(col)
      column = []
      @board.each {|x| column << x[col] }
      return column
    end

    def get_row(row)
      return @board[row]
    end 

    def get_diagonal
      (0...@board[0].size).map {|x| @board[x][x]}
    end             
  
end

dice_grid = [["b", "r", "a", "e"],
             ["i", "o", "d", "t"],
             ["e", "c", "l", "r"],
             ["t", "a", "k", "e"]]

boggle_board = BoggleBoard.new(dice_grid)

# implement tests for each of the methods here:

p boggle_board.create_word(dice_grid, [1,2], [1,1], [2,1], [3,2]) #=> "dock"
puts boggle_board.get_col(0).to_s #=> ["b", "i", "e", "t"]
puts boggle_board.get_col(1).to_s #=> ["r", "o", "c", "a"]
puts boggle_board.get_col(2).to_s #=> ["a", "d", "l", "k"]
puts boggle_board.get_col(3).to_s #=> ["e", "t", "r", "e"]
puts boggle_board.get_row(0).to_s #=> ["b", "r", "a", "e"]
puts boggle_board.get_row(1).to_s #=> ["i", "o", "d", "t"]
puts boggle_board.get_row(2).to_s #=> ["e", "c", "l", "r"]
puts boggle_board.get_row(3).to_s #=> ["t", "a", "k", "e"]


# create driver test code to retrieve a value at a coordinate here:

p boggle_board.create_word(dice_grid,[3,2]) #=> k
```