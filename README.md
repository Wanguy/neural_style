# neural_style

Simplified Chinese Documentation

An implementation of [neural style](http://arxiv.org/pdf/1508.06576v2.pdf) in TensorFlow.

TensorFlow doesn't support [L-BFGS](https://en.wikipedia.org/wiki/Limited-memory_BFGS) (which is what the original authors used), so we use [Adam](http://arxiv.org/abs/1412.6980). This may require a little bit more hyperparameter tuning to get nice results.

## Related Projects

See [here](https://github.com/lengstrom/fast-style-transfer) for an implementation of [fast (feed-forward) neural style](https://arxiv.org/pdf/1603.08155v1.pdf) in TensorFlow.

## Requirements

### Dependencies

You can install Python dependencies using `pip install -r requirements.txt`, and it should just work. If you want to install the packages manually, here's a list:

- [TensorFlow](https://www.tensorflow.org/versions/master/get_started/os_setup.html#download-and-setup)
- [H5PY](http://www.h5py.org/)
- [Pillow](http://pillow.readthedocs.io/en/3.3.x/installation.html#installation)
- [Kera](https://keras.io/)
- [Deep learning model](https://github.com/fchollet/deep-learning-models)

## Running

`python neural_style_transfer.py "<content file>" "<style file>" "<output file>"`

> `<output file>` no extension is required.

Run `python neural_style.py --help` to see a list of all options.

Use `--checkpoint-output` and `--checkpoint-iterations` to save checkpoint images.

## License

Copyright (c) 2015-2017 Anish Athalye. Released under GPLv3. See [LICENSE.txt](https://github.com/Wanguy/neural_style/blob/master/LICENSE) for details.