# dart-midterm-output

import 'dart:math';
import 'dart:io';


void main() {

int botscore=0;
int yourscore=0;
int round= 1;

for( var i = 3; i >= 1; i-- )

{
String randomNumber() {
  Random random = new Random();
  int rand = random.nextInt(3); 
  
  switch (rand) {
    case 0:
      return "Bato";
      break;
    case 1:
      return "Papel";
      break;
    case 2:
      return "Gunting";
      break;
    default:
      break;
  }
}

    print ('ROUND $round');
    print('Papel, Gunting, Bato. Whats your pick?');
   

String pambato= stdin.readLineSync();

print ('------------------');


if(pambato == 'bato'|| pambato== 'Bato')
{
if(randomNumber==1)
{
print( '$pambato vs Gunting ');
print ('You Win');
yourscore = yourscore+1;
}
else if(randomNumber==2)
{
print( '$pambato vs Bato ');
print ('Tie');
}
else
{
print( '$pambato vs Papel ');
print ('You Lose');
botscore= botscore+1;
}
}


if(pambato == 'gunting'|| pambato== 'Gunting')
{
if(randomNumber==1)
{
print( '$pambato vs Gunting ');
print ('Tie');
}
else if(randomNumber==2)
{
print( '$pambato vs Bato ');
print ('You Lose');
botscore= botscore+1;
}
else
{
print( '$pambato vs Papel ');
print ('You Win');
yourscore= yourscore+1;
}
}


if(pambato == 'papel'|| pambato== 'Papel')
{
if(randomNumber==1)
{
print( '$pambato vs Gunting ');
print ('You Lose');
botscore= botscore+1;
}
else if(randomNumber==2)
{
print( '$pambato vs Bato ');
print ('You Win');
yourscore= yourscore+1;
}
else
{
print( '$pambato vs Papel ');
print ('Tie ');
}
}


round=round+1;
String rand = randomNumber();
print("Bot played $rand");
print ('------------------');
print('Bot score: $botscore' );
print('Your score: $yourscore' );
print ('''***************


''');


}
}
