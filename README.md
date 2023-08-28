# arrays-strings-coding-questons

Counting Valleys

An avid hiker keeps meticulous records of their hikes. During the last hike that took exactly  steps, for every step it was noted if it was an uphill, , or a downhill,  step. Hikes always start and end at sea level, and each step up or down represents a  unit change in altitude. We define the following terms:

A mountain is a sequence of consecutive steps above sea level, starting with a step up from sea level and ending with a step down to sea level.
A valley is a sequence of consecutive steps below sea level, starting with a step down from sea level and ending with a step up to sea level.
Given the sequence of up and down steps during a hike, find and print the number of valleys walked through.

Sample Input

8
UDDDUDUU
Sample Output

1


function countingValleys(steps, path) {
    // Write your code here
   let altitude = 0; 
    
    let valleys = 0; 
    let isInValley = false; 
    
    for(let i=0;i<path.length;i++){
      if(path[i] === 'U'){
        altitude++;
      }
        else if(path[i] === 'D') {
            altitude--;
        }
        
   if(altitude === -1 ){
      isInValley=true;
   }
        
        else if(altitude === 0 && isInValley){
          valleys++;
            isInValley=false;
        }
        
        
    }
    return valleys;

}

