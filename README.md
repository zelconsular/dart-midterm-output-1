import 'dart:math';
import 'dart:io'; 



void main() {


int score=0;
int round= 1;

for( var i = 3; i >= 1; i-- ) 
{
Random random = new Random();
int randomNumber = random.nextInt(3)+(1); 
print ('round $round');
print('Gunting, Papel,Bato.');
print ('Ano ang inyong pambato?');
String pambato= stdin.readLineSync(); 
print ('--------------------');

   if(pambato == 'bato'|| pambato== 'Bato')
      {
        if(randomNumber==1)
        {
         print( '$pambato vs Gunting ');
          print ('You Win');
          score = score+1;
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
        }
        else
        {
          print( '$pambato vs Papel ');
          print ('You Win');
          score=score+1;
        }
      }
if(pambato == 'papel'|| pambato== 'Papel')
      {
        if(randomNumber==1)
        {
          print( '$pambato vs Gunting ');
          print ('You Lose');
        }
        else if(randomNumber==2)
        {
          print( '$pambato vs Bato ');
          print ('You Win');
          score=score+1;
        }
        else
        {
          print( '$pambato vs Papel ');
          print ('Tie ');
        }
      }  
round=round+1;
print ('--------------------');
print('score $score' );
print ('--------------------');
}
}
