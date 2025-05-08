# X-O

** let currentPlayer = "X";<---- Zawsze jest pierwsza tura x 
        let gameBoard = ["", "", "", "", "", "", "", "", ""]; <---wszystkie pola 
        let winningCombo = [0, 0, 0]; <--- kombo dla wygrania
        let gameOver = false;  
**  

To jest linia ktora idzie od 0 do 2 itp   

      function drawWinningLine() {
            const line = document.createElement("div");
            line.classList.add("line");
            board.appendChild(line);

            const [start, , end] = winningCombo;

            if (start === 0 && end === 2) {
                line.style.width = "312px";
                line.style.top = "50px";
                line.style.left = "0";
            } else if (start === 3 && end === 5) {
                line.style.width = "312px";
                line.style.top = "160px";
                line.style.left = "0";
            } else if (start === 6 && end === 8) {
                line.style.width = "312px";
                line.style.top = "267px";
                line.style.left = "0";
            } else if (start === 0 && end === 6) {
                line.style.width = "320px";
                line.style.top = "0";
                line.style.left = "55px";
                line.style.transform = "rotate(90deg)";
            } else if (start === 1 && end === 7) {
                line.style.width = "320px";
                line.style.top = "";
                line.style.left = "160px";
                line.style.transform = "rotate(90deg)";
            } else if (start === 2 && end === 8) {
                line.style.width = "320px";
                line.style.top = "0";
                line.style.left = "265px";
                line.style.transform = "rotate(90deg)";
            } else if (start === 0 && end === 8) {
                line.style.width = "440px";
                line.style.top = "0";
                line.style.left = "0";
                line.style.transform = "rotate(45deg)";
            } else if (start === 2 && end === 6) {
                line.style.width = "447px";
                line.style.top = "0";
                line.style.left = "315px";
                line.style.transform = "rotate(134deg)";}
            }


! <--- to jesst wsszystkie kombo dla wygrania w X-O

  function checkWin() {
            const winConditions = [
                [0,1,2],   
                [3,4,5],    
                [6,7,8],     
                [0,3,6],   
                [1,4,7],   
                [2,5,8],  
                [0,4,8],   
                [2,4,6],   
            ];

            for (const condition of winConditions) {
                const [a, b, c] = condition;
                if (
                    gameBoard[a] &&
                    gameBoard[a] === gameBoard[b] &&
                    gameBoard[a] === gameBoard[c]
                ) {
                    winningCombo = condition;
                    return true;
                }
                
            }
            return false;
        }


            
    
