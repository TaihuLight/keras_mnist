# Keras MNIST

Just in case this ever stops working:

```python
import os
import hashlib
import tensorflow as tf
keras = tf.contrib.keras

(x_train, y_train), (x_test, y_test) = keras.datasets.mnist.load_data()

mnist_path = '~/.keras/datasets/mnist.npz'
mnist_path_full = os.path.expanduser(mnist_path)
mnist_md5 = hashlib.md5(open(mnist_path_full).read()).hexdigest()
mnist_md5_expected = '8a61469f7ea1b51cbae51d4f78837e45'
assert mnist_md5 == mnist_md5_expected
```
