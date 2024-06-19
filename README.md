## Photo Mosaic Using golang 
This is algorithm for creating Photo Mosaic using golang.  
 - Following steps has been followed without use of any third party library
    - Build a database, a hash for tile pictures, by scanning a directory of pictures and then using the filename as the key and the average color of the pictures as the value.
    - Average color is three tuple color namely Red, Green, Blue of every pixel and adding up all the reds, greens, and blues, and then dividing by the total number of pixels.
    - Cut the target picture into smaller pictures of the correct tile size.  
    - Assume the average color to be the color of the top-left pixel of that piece.  
    - Find nearest match of piece to tiles that was calculated before using Eclidean distance between the two color 3-tuples by converting each color 3 tuple into a point in a 3-dimensional space.  
    - Remove the tile from the database so that each tile in the photo mosaic is unique.

 - This algorithm utilizes concurrency for processing the divided target image into 4 parts and then pushing each to channels to merge them into one and getting the final image, this approach is much efficient as 
   compared to sequential approach, where this process takes approx 2 seconds but with help of concurrency it takes only around approx 800ms.
   
 - Steps involved
   - Split the original Image into four parts
   - Process them at the same time ( Concurrency )
   - Combine the Results into a single mosaic

### Note :-  
- You Just need to Execute the learn.exe file on you system with ```tiles``` as folder and should contain all the images for Mosaic.

## Test Run  
Standing Elephant
- Dimensions :- 427 X 640
- Size :- 60 KB
- Number of pixels :- 10
- Time Taken at time of test :- Approx 25 ms

![image](https://github.com/CaptainTron/Photo-Mosaic-Algo/assets/94986377/4f7b65f7-9d25-421e-8992-992d5631f158)
