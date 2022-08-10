The parse representations method is generally called a method in which we perform a series of analyzes on the representation we have. We are going to convert it into multi-dimensional arrays, in the form of a matrix. If I want to explain better, we will consider each of these arrays as a signal for our image. Now, what we will do with these signals depends on our project. (The reason for regression is a method of recognizing that now there is no difference in our input data.) Let's create a special order in our signals using the dictionaries that exist for this method. This special order is such that we use a certain coefficient We use very small domains in our matrices. Now, because these changes we gave are only local changes, we will enlarge the domain of the coefficients that we used with the mathematical methods of rolling, but we will not apply these changes to the previous coefficients, we will determine them in their neighborhood. For example, consider two circles that are inside the same circle. Small domains become large circles. There are non-linearities, which are small, but they still create a lot of space in the domain of the main functions, which is what we do with this. It happens that the location of these edges has a specific geometric order, so we use their display in our dictionary. Now, when we have determined the values ​​of these dictionaries in this way, we use this dictionary to place all our signals under the radius, but then again. There are some small approximations that are named as theta t, they are almost the direction of our dictionary. Now if you look at the code, our main functions are exactly like this:

show_im

show_imgs_results

del_patch

get_patch

fill_patch

naive_high_priority_pixel

get_boundary_pixels

get_dictionary

The first two functions have nothing to do with our work
 The next three functions are related to the division of our signals, one takes, one erases, and one fills
The next function identifies the signals with higher priority and finds them
The next function comes to find the signal created by demarcation
The next function is to create our dictionary using the same data, just pay attention to the value of our dictionary at the beginning of the work.
The next function is Inpainting, where we apply the dictionary to all the signals in the image
- Now, the application of this case is that, for example, we have an image that has a damaged part, so we cannot use this method on it, we will use deep and machine learning methods to work on a healthy image with the same details of the damaged image. It reconstructs the visual damage image using our model that we trained it
