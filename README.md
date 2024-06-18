### Photo Mosaic Using golang 
This is algorithm for creating Photo Mosaic using golang.  
 - This algorithm utilizes concurrency for processing the divided target image into 4 parts and then pushing each to channels to merge them into one and getting the final image, this approach is much efficient as compared to sequential approach, where this process takes approx 2 seconds seconds but with help of concurrency it takes only around approx 800ms.  
