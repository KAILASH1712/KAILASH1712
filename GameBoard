import java.util.Arrays;
import java.util.Collections;
import java.util.List;

public class GameBoard {
    private int[][] board;
    private final int size = 4; 

    public GameBoard() {
        initializeBoard();
        shuffleBoard();
    }

    private void initializeBoard() {
        board = new int[size][size];
        int num = 1;
        for (int i = 0; i < size; i++) {
            for (int j = 0; j < size; j++) {
                board[i][j] = num++;
            }
        }
        
        board[size - 1][size - 1] = 0;
    }

    private void shuffleBoard() {
        Integer[] flatBoard = new Integer[size * size];
        int index = 0;
        for (int i = 0; i < size; i++) {
            for (int j = 0; j < size; j++) {
                flatBoard[index++] = board[i][j];
            }
        }
        List<Integer> list = Arrays.asList(flatBoard);
        Collections.shuffle(list.subList(0, list.size() - 1));

        index = 0;
        for (int i = 0; i < size; i++) {
            for (int j = 0; j < size; j++) {
                board[i][j] = list.get(index++);
            }
        }
    }

    public void printBoard() {
        for (int i = 0; i < size; i++) {
            for (int j = 0; j < size; j++) {
                System.out.print(board[i][j] + "\t");
            }
            System.out.println();
        }
    }

    public static void main(String[] args) {
        GameBoard game = new GameBoard();
        game.printBoard();
    }
}
****
