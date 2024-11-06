# temp
PASS-1 OF TWO-PASS ASSEMBLER

class Pass1

{

public static void main(String args[])

{

int c = 0;

String[][] symbolTable = {{" ", "START", "101", " "}, {" ", "MOVER", "BREG", " "}, {"AGAIN", 

"MULT", "BREG", "TERM"}, {" ", "MOVER", "CREG", "TERM"}, {" ", "ADD", "CREG", "N"}, {" ", 

"MOVEM", "CREG", "TERM"}, {"N", "DS", "2", " "}, {"RESULT", "DS", "2", " "}, {"ONE", "DC", "1", " "}, 

{"TERM", "DC", "1", " "}, {" ", "END", " ", " "}};

System.out.println("\n\t********SYMBOL TABLE********");

System.out.println("\t____________________________");

int i = 0;

int j = 0;

for (i=0; i<symbolTable.length; i++)

{ 

for (j=0; j<symbolTable[i].length; j++)

{

System.out.print("\t" + symbolTable[i][j]);

}

System.out.print("\n");

}

System.out.print("\n");

System.out.print("\n");

int k = 0;

int l = 0;

for (k=0; k<symbolTable.length; k++)

{

if (symbolTable[k][0] != " ")

{

c += 1;

for (l=0; l<symbolTable[0].length; l++)
{

System.out.print("\t" + symbolTable[k][l]);

}

System.out.print("\n");

}

}

System.out.println("\nCounter: " + c + "\n");

}}

OUTPUT :

 ********SYMBOL TABLE********

 ____________________________

 START

101 

 MOVER

BREG 

 AGAIN MULT 

BREG TERM

 MOVER

CREG TERM

 ADD

CREG N 

 MOVEM

CREG TERM

 N DS 

2

 RESULT DS 

2

 ONE DC 

1

 TERM DC 

1

 END 

 AGAIN MULT 

BREG TERM

 N DS 

2

 RESULT DS 

2

 ONE DC 

1

 TERM DC 

1

Counter: 5
