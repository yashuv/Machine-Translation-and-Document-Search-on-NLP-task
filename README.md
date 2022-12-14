## Machine Translation and Document Search

Machine translation is a technology that is used to automatically translate text from one language to another.*For example*, if you are looking for documents written in French, you can use a machine translation tool to translate the documents into English.  It is a rapidly evolving field that is used in a variety of applications, including online translation services, software localization, and automatic document search. There are a variety of different approaches that are used to achieve this goal.

We will learn to transform word vectors and assign them to subsets using locality sensitive hashing, in order to perform machine translation and document search.

I achieved the following learning goals:
* Gradient descent
* Approximate nearest neighbors
* Locality sensitive hashing
* Hash functions
* Hash tables
* K nearest neighbors
* Document search
* Machine translation
* Frobenius norm

### Transforming word vectors
In the previous week, we have seen how we can plot word vectors. Now, we will see how you can take a word vector and learn a mapping that will allow you to translate words by learning a "transformation matrix". Here is a visualization:

<img src="images/transforming word vectors.jpg">

Note that the word "chat" in french means cat. You can learn that by taking the  vector corresponding to "cat" in english, multiplying it by a matrix that you learn and then you can use cosine similarity between the output and all the french vectors. You should see that the closest result is the vector which corresponds to "chat".

Here is a visualization of that showing you the aligned vectors: 

<img src="images/visualization of aligned vectors.jpg">

Note that XX corresponds to the matrix of english word vectors and YY corresponds to the matrix of french word vectors. RR is the mapping matrix.

<img src="images/steps to learn R.jpg">

Here is an example to show you how the frobenius norm works.

<img src="images/forbenius norm.png">

## Linear Transformation: Rotation of matrix in R²
A rotation matrix is a matrix that is used to perform a rotation in linear algebra. It is a real square matrix whose transpose is also its inverse.<br>
Let  R<sub>θ</sub>:R²→R² be a linear transformation given by rotating vector v<sub>0</sub> by a counterclockwise angle θ in a fixed coordinate system. Then the rotation matrix R<sub>θ</sub> is given by:

<img src="images/steps to learn R.jpg">

so
		v<sup>'</sup> = R<sub>θ</sub>v<sub>0</sub>.
    
It means that if we want to rotate a vector v<sub>0</sub>  with the coordinates (x, y) then we use matrix multiplication to perform the rotation as follows:

<img src="images/showing transformation in matrix form.jpg">

The rotation is shown in the diagram below:

<img src="images/diagram of rotation in R2.jpg">

## k nearest neighbors
The intuition behind the k nearest neighbors is that it allows us to find points in space that are close to our data point of interest, and then use those points to make predictions about our data point of interest. We previously used it to find out the similar word vector in our corpus.<br>
But there are a few potential disadvantages of finding a matching word by finding the k nearest neighbors of a vector. One is that the vector may not be representative of the entire word, so the nearest neighbors may not be very similar to the word. Another is that  it requires a lot of computation to find the nearest neighbors for each point in the dataset. This can be expensive and slow if the dataset is large.<br>
Hence, it is often used in conjunction with other more efficient algorithms. 

##  Hash tables and Hash Functions
Hash tables are used to store data in a way that makes it easier and faster to look up and retrieve, which is helpful when using k nearest neighbors. It is a useful data structure for storing key-value pairs that can be used in a very efficient way. The key is used to access the data, and the value is the data that is stored. <br>
A function that assigns a hash value is called a *hash function*. The intuition behind a hash function is that it takes some arbitrary sized data and converts it into a fixed size value that identifies the data. Hash functions are used in hash tables, checksums, cryptographic hash functions, fingerprinting, and other applications.

<img src="images/example of a hash function.jpg">

The diagram above shows a concrete example of a hash function which takes a vector and returns a value. Then you can mod that value by the number of buckets and put that number in its corresponding bucket. For example, 14 is in the 4th bucker, 17 & 97 are in the 7th bucket. 

## Locality sensitive hashing
Locality sensitive hashing is a technique that allows you to hash similar inputs into the same buckets with high probability. Locality is another word for "location", and sensitive is another word for "caring." So locality sensitive hashing is a hashing method that cares very deeply about assigning items based on where they’re located in vector space.<br>
It is useful because it can allow for approximate nearest neighbor search in high dimensional spaces that would otherwise be too computationally expensive. It is also relatively simple to implement. LSH is used in many applications, such as content-based image retrieval, collaborative filtering, and spell-checking.

## Approximate nearest neighbors
Approximate nearest neighbors is a method of finding the nearest neighbors of a given data point in a dataset. It is an efficient method of finding the nearest neighbors of a given data point, especially when the dataset is large.It is a form of dimensionality reduction that can be used to speed up searches and make them more efficient. <br>
It does not give you the full nearest neighbors but gives you an approximation of the nearest neighbors. It usually trades off accuracy for efficiency.

<img src="images/approximate nearest neighbors.jpg">

You are trying to find the nearest neighbor for the red vector (point). The first time, the plane gave you green points. You then ran it a second time, but this time you got the blue points. The third time you got the orange points to be the neighbors. So you can see as you do it more times, you are likely to get all the neighbors.

## Document search
We can actually represent a document as a vector. Vector space models represent documents as vectors in a high-dimensional space, and they can be used to find similar documents or to cluster documents together. <br>
In our programming example, we just added the word vectors of a document to get the document vector. 

### Conclusion
I learned to transform word vectors and assign them to subsets using *locality sensitive hashing*, in order to perform machine translation and document search.<br>
I had the opportunity to apply all of the aforementioned concepts and skills into practice. It was a fantastic learning experience. I appreciate and am grateful for the chance.

Thank you, and happy learning!<br>
***