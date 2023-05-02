Training
==============

By default
`python tools/train.py <https://gitlab-icv.inn.intel.com/algo_rnd_team/anomaly/blob/samet/stfpm/tools/train.py>`__
runs `PADIM <https://arxiv.org/pdf/2011.08785.pdf>`__ model
`MVTec AD <https://www.mvtec.com/company/research/datasets/mvtec-ad>`__
``leather`` dataset.

.. code-block:: bash

    python tools/train.py    # Train PADIM on MVTec AD leather

Training a model on a specific dataset and category requires further
configuration. Each model has its own configuration file,
`config.yaml <https://gitlab-icv.inn.intel.com/algo_rnd_team/anomaly/blob/samet/stfpm/anomalib/models/stfpm/config.yaml>`__,
which contains data, model and training configurable parameters. To
train a specific model on a specific dataset and category, the config
file is to be provided:

.. code-block:: bash

    python tools/train.py --config <path/to/model/config.yaml>

Alternatively, a model name could also be provided as an argument, where
the scripts automatically finds the corresponding config file.

.. code-block:: bash

    python tools/train.py --model padim

To see a list of currently supported models, refer to page: :ref:`available models`
