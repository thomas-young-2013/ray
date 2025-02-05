
.. include:: /_includes/rllib/we_are_hiring.rst

.. include:: /_includes/rllib/new_api_stack.rst

.. _utils-reference-docs:

RLlib Utilities
===============

Here is a list of all the utilities available in RLlib.

Exploration API
---------------

Exploration is crucial in RL for enabling a learning agent to find new, potentially high-reward states by reaching unexplored areas of the environment.

RLlib has several built-in exploration components that
the different algorithms use. You can also customize an algorithm's exploration
behavior by sub-classing the Exploration base class and implementing
your own logic:

Built-in Exploration components
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. currentmodule:: ray.rllib.utils.exploration

.. autosummary::
   :nosignatures:
   :toctree: doc/

   ~exploration.Exploration
   ~random.Random
   ~stochastic_sampling.StochasticSampling
   ~epsilon_greedy.EpsilonGreedy
   ~gaussian_noise.GaussianNoise
   ~ornstein_uhlenbeck_noise.OrnsteinUhlenbeckNoise
   ~random_encoder.RE3
   ~curiosity.Curiosity
   ~parameter_noise.ParameterNoise


Inference
~~~~~~~~~
.. autosummary::
   :nosignatures:
   :toctree: doc/

   ~exploration.Exploration.get_exploration_action

Callback hooks
~~~~~~~~~~~~~~

.. autosummary::
   :nosignatures:
   :toctree: doc/

   ~exploration.Exploration.before_compute_actions
   ~exploration.Exploration.on_episode_start
   ~exploration.Exploration.on_episode_end
   ~exploration.Exploration.postprocess_trajectory


Setting and getting states
~~~~~~~~~~~~~~~~~~~~~~~~~~

.. autosummary::
   :nosignatures:
   :toctree: doc/

   ~exploration.Exploration.get_state
   ~exploration.Exploration.set_state



Scheduler API
-------------

Use a scheduler to set scheduled values for variables (in Python, PyTorch, or
TensorFlow) based on an (int64) timestep input. The computed values are usually float32
types.




Built-in Scheduler components
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. currentmodule:: ray.rllib.utils.schedules

.. autosummary::
   :nosignatures:
   :toctree: doc/

   ~schedule.Schedule
   ~constant_schedule.ConstantSchedule
   ~linear_schedule.LinearSchedule
   ~piecewise_schedule.PiecewiseSchedule
   ~exponential_schedule.ExponentialSchedule
   ~polynomial_schedule.PolynomialSchedule

Methods
~~~~~~~

.. autosummary::
   :nosignatures:
   :toctree: doc/

   ~schedule.Schedule.value
   ~schedule.Schedule.__call__


.. _train-ops-docs:

Training Operations Utilities
-----------------------------

.. currentmodule:: ray.rllib.execution.train_ops

.. autosummary::
   :nosignatures:
   :toctree: doc/

   ~multi_gpu_train_one_step
   ~train_one_step


Framework Utilities
-------------------

Import utilities
~~~~~~~~~~~~~~~~

.. currentmodule:: ray.rllib.utils.framework

.. autosummary::
   :nosignatures:
   :toctree: doc/

   ~try_import_torch
   ~try_import_tf
   ~try_import_tfp


Tensorflow utilities
~~~~~~~~~~~~~~~~~~~~

.. currentmodule:: ray.rllib.utils.tf_utils

.. autosummary::
   :nosignatures:
   :toctree: doc/

   ~explained_variance
   ~flatten_inputs_to_1d_tensor
   ~get_gpu_devices
   ~get_placeholder
   ~huber_loss
   ~l2_loss
   ~make_tf_callable
   ~minimize_and_clip
   ~one_hot
   ~reduce_mean_ignore_inf
   ~scope_vars
   ~warn_if_infinite_kl_divergence
   ~zero_logps_from_actions


Torch utilities
~~~~~~~~~~~~~~~

.. currentmodule:: ray.rllib.utils.torch_utils


.. autosummary::
   :nosignatures:
   :toctree: doc/

   ~apply_grad_clipping
   ~concat_multi_gpu_td_errors
   ~convert_to_torch_tensor
   ~explained_variance
   ~flatten_inputs_to_1d_tensor
   ~global_norm
   ~huber_loss
   ~l2_loss
   ~minimize_and_clip
   ~one_hot
   ~reduce_mean_ignore_inf
   ~sequence_mask
   ~warn_if_infinite_kl_divergence
   ~set_torch_seed
   ~softmax_cross_entropy_with_logits


Numpy utilities
~~~~~~~~~~~~~~~

.. currentmodule:: ray.rllib.utils.numpy

.. autosummary::
   :nosignatures:
   :toctree: doc/

   ~aligned_array
   ~concat_aligned
   ~convert_to_numpy
   ~fc
   ~flatten_inputs_to_1d_tensor
   ~make_action_immutable
   ~huber_loss
   ~l2_loss
   ~lstm
   ~one_hot
   ~relu
   ~sigmoid
   ~softmax

Checkpoint utilities
~~~~~~~~~~~~~~~~~~~~

.. currentmodule:: ray.rllib.utils.checkpoints

.. autosummary::
   :nosignatures:
   :toctree: doc/

   Checkpointable
   convert_to_msgpack_checkpoint
   convert_to_msgpack_policy_checkpoint
   get_checkpoint_info
   try_import_msgpack

Policy utilities
~~~~~~~~~~~~~~~~

.. currentmodule:: ray.rllib.utils.policy

.. autosummary::
   :nosignatures:
   :toctree: doc/

   compute_log_likelihoods_from_input_dict
   create_policy_for_framework
   local_policy_inference
   parse_policy_specs_from_checkpoint

Other utilities
~~~~~~~~~~~~~~~

.. currentmodule:: ray.rllib.utils

.. autosummary::
   :nosignatures:
   :toctree: doc/

   tensor_dtype.get_np_dtype
