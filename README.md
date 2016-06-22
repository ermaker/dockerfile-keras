# dockerfile-keras

Dockerized [Keras] with [Theano] and [TensorFlow].

## Get Started

Run an example:

```sh
docker run --rm -it ermaker/keras sh -c 'curl -sSL https://github.com/fchollet/keras/raw/master/examples/mnist_mlp.py | python'
```

Run [Keras] with [TensorFlow]: (See [this][Keras Backend] for more information)

```sh
docker run --rm -it -e KERAS_BACKEND=tensorflow ermaker/keras sh -c 'curl -sSL https://github.com/fchollet/keras/raw/master/examples/mnist_mlp.py | python'
```

Check the backend:

```sh
docker run --rm -it -e KERAS_BACKEND=tensorflow ermaker/keras python -c "from keras import backend; print backend._BACKEND"
```

Run your script:

```sh
docker run --rm -it -v $(pwd)/YOUR_SCRIPT.py:/YOUR_SCRIPT.py:ro ermaker/keras python YOUR_SCRIPT.py
```

[Keras]: http://keras.io/
[Theano]: http://deeplearning.net/software/theano/
[TensorFlow]: https://www.tensorflow.org/
[Keras Backend]: http://keras.io/backend/
