
# (k-NN)
we aim to implement an algorithm called **k-Nearest Neighbors (k-NN)**, which is one of the common machine learning algorithms.
[More about k-NN algorithm](https://en.wikipedia.org/wiki/K-nearest_neighbors_algorithm)

a well-known dataset called [Iris Flower](https://en.wikipedia.org/wiki/Iris_flower_data_set) is provided, containing the characteristics of 150 iris flowers. Each of these flowers belongs to one of the three iris types: Setosa (Iris setosa), Versicolor (Iris versicolor), and Virginica (Iris virginica). The characteristics of each flower include the length and width of both sepals and petals. By using these characteristics, we can consider each flower as a point in a four-dimensional space, where these four quantities determine the coordinates of that point.

The characteristics of 120 iris flowers are stored in a file named `irises.npy`. When this file is read, it creates a 120x4 array, where each row represents the characteristics of a flower (sepal length, sepal width, petal length, and petal width in centimeters).

On the other hand, the types of these flowers (Setosa, Versicolor, or Virginica) are stored numerically in another file named `types.npy`. The values in this array are represented as `0`, `1`, or `2`, indicating the types respectively as Setosa, Versicolor, and Virginica.

we are to implement an algorithm that, given the characteristics of an iris flower, predicts its type. This prediction will be made using samples for which we already know their types, i.e., the data we have read before. From now on, we will refer to these samples as **training samples**.

The characteristics of another set of 30 iris flowers, for which we **do not know their types** and are expected to predict using the k-NN algorithm, are provided in another file named `new_irises.npz`. When this file is read, it creates a 30x4 array, where each row represents the characteristics of a flower. We will refer to these samples as **testing samples**.

### The steps of this algorithm are as follows:

1. **Calculate the distance:** First, calculate the distance between the test sample (the sample for which we intend to predict the type) and all training samples (samples for which we already know the type).

2. **Find the nearest k training samples:** Identify the k training samples that have the smallest distances to our test sample.

3. **Determine the predicted type:** Examine which type is the most common among these k samples. Declare that type as our prediction for the test sample.

The algorithm aims to predict the type of the test sample based on the types of the nearest neighbors among the training samples.

