```
python model_main.py --logtostderr --train_dir=/Users/home/Documents/Tensorflow/workspace/training_demo/training/ --pipeline_config_path=/Users/home/Documents/Tensorflow/workspace/training_demo/training/ssd_inception_v2_coco.config


WARNING: The TensorFlow contrib module will not be included in TensorFlow 2.0.
For more information, please see:
  * https://github.com/tensorflow/community/blob/master/rfcs/20180907-contrib-sunset.md
  * https://github.com/tensorflow/addons
If you depend on functionality not listed there, please file an issue.

WARNING:tensorflow:Forced number of epochs for all eval validations to be 1.
WARNING:tensorflow:Expected number of evaluation epochs is 1, but instead encountered `eval_on_train_input_config.num_epochs` = 0. Overwriting `num_epochs` to 1.
WARNING:tensorflow:Using temporary folder as model directory: /var/folders/79/kr9h3xf94f7fkghw3f9tky5h0000gn/T/tmp4nkq9mnk
WARNING:tensorflow:Estimator's model_fn (<function create_model_fn.<locals>.model_fn at 0x1c35f39730>) includes params argument, but params are not passed to Estimator.
WARNING:tensorflow:From /anaconda3/lib/python3.7/site-packages/tensorflow/python/framework/op_def_library.py:263: colocate_with (from tensorflow.python.framework.ops) is deprecated and will be removed in a future version.
Instructions for updating:
Colocations handled automatically by placer.
WARNING:tensorflow:num_readers has been reduced to 1 to match input file shards.
WARNING:tensorflow:From /Users/home/Documents/TensorFlow/models/research/object_detection/builders/dataset_builder.py:86: parallel_interleave (from tensorflow.contrib.data.python.ops.interleave_ops) is deprecated and will be removed in a future version.
Instructions for updating:
Use `tf.data.experimental.parallel_interleave(...)`.
WARNING:tensorflow:From /Users/home/Documents/TensorFlow/models/research/object_detection/core/preprocessor.py:188: sample_distorted_bounding_box (from tensorflow.python.ops.image_ops_impl) is deprecated and will be removed in a future version.
Instructions for updating:
`seed2` arg is deprecated.Use sample_distorted_bounding_box_v2 instead.
WARNING:tensorflow:From /Users/home/Documents/TensorFlow/models/research/object_detection/builders/dataset_builder.py:158: batch_and_drop_remainder (from tensorflow.contrib.data.python.ops.batching) is deprecated and will be removed in a future version.
Instructions for updating:
Use `tf.data.Dataset.batch(..., drop_remainder=True)`.
WARNING:tensorflow:From /anaconda3/lib/python3.7/site-packages/tensorflow/python/ops/losses/losses_impl.py:448: to_float (from tensorflow.python.ops.math_ops) is deprecated and will be removed in a future version.
Instructions for updating:
Use tf.cast instead.
WARNING:tensorflow:From /anaconda3/lib/python3.7/site-packages/tensorflow/python/ops/array_grad.py:425: to_int32 (from tensorflow.python.ops.math_ops) is deprecated and will be removed in a future version.
Instructions for updating:
Use tf.cast instead.
2019-06-14 21:17:57.769289: I tensorflow/core/platform/cpu_feature_guard.cc:141] Your CPU supports instructions that this TensorFlow binary was not compiled to use: AVX2 FMA
Traceback (most recent call last):
  File "/anaconda3/lib/python3.7/site-packages/tensorflow/python/client/session.py", line 1334, in _do_call
    return fn(*args)
  File "/anaconda3/lib/python3.7/site-packages/tensorflow/python/client/session.py", line 1319, in _run_fn
    options, feed_dict, fetch_list, target_list, run_metadata)
  File "/anaconda3/lib/python3.7/site-packages/tensorflow/python/client/session.py", line 1407, in _call_tf_sessionrun
    run_metadata)
tensorflow.python.framework.errors_impl.InvalidArgumentError: assertion failed: [Unable to decode bytes as JPEG, PNG, GIF, or BMP]
	 [[{{node case/cond/cond_jpeg/decode_image/cond_jpeg/cond_png/cond_gif/Assert_1/Assert}}]]
	 [[{{node IteratorGetNext}}]]

During handling of the above exception, another exception occurred:

Traceback (most recent call last):
  File "model_main.py", line 109, in <module>
    tf.app.run()
  File "/anaconda3/lib/python3.7/site-packages/tensorflow/python/platform/app.py", line 125, in run
    _sys.exit(main(argv))
  File "model_main.py", line 105, in main
    tf.estimator.train_and_evaluate(estimator, train_spec, eval_specs[0])
  File "/anaconda3/lib/python3.7/site-packages/tensorflow_estimator/python/estimator/training.py", line 471, in train_and_evaluate
    return executor.run()
  File "/anaconda3/lib/python3.7/site-packages/tensorflow_estimator/python/estimator/training.py", line 611, in run
    return self.run_local()
  File "/anaconda3/lib/python3.7/site-packages/tensorflow_estimator/python/estimator/training.py", line 712, in run_local
    saving_listeners=saving_listeners)
  File "/anaconda3/lib/python3.7/site-packages/tensorflow_estimator/python/estimator/estimator.py", line 358, in train
    loss = self._train_model(input_fn, hooks, saving_listeners)
  File "/anaconda3/lib/python3.7/site-packages/tensorflow_estimator/python/estimator/estimator.py", line 1124, in _train_model
    return self._train_model_default(input_fn, hooks, saving_listeners)
  File "/anaconda3/lib/python3.7/site-packages/tensorflow_estimator/python/estimator/estimator.py", line 1158, in _train_model_default
    saving_listeners)
  File "/anaconda3/lib/python3.7/site-packages/tensorflow_estimator/python/estimator/estimator.py", line 1407, in _train_with_estimator_spec
    _, loss = mon_sess.run([estimator_spec.train_op, estimator_spec.loss])
  File "/anaconda3/lib/python3.7/site-packages/tensorflow/python/training/monitored_session.py", line 676, in run
    run_metadata=run_metadata)
  File "/anaconda3/lib/python3.7/site-packages/tensorflow/python/training/monitored_session.py", line 1171, in run
    run_metadata=run_metadata)
  File "/anaconda3/lib/python3.7/site-packages/tensorflow/python/training/monitored_session.py", line 1270, in run
    raise six.reraise(*original_exc_info)
  File "/anaconda3/lib/python3.7/site-packages/six.py", line 693, in reraise
    raise value
  File "/anaconda3/lib/python3.7/site-packages/tensorflow/python/training/monitored_session.py", line 1255, in run
    return self._sess.run(*args, **kwargs)
  File "/anaconda3/lib/python3.7/site-packages/tensorflow/python/training/monitored_session.py", line 1327, in run
    run_metadata=run_metadata)
  File "/anaconda3/lib/python3.7/site-packages/tensorflow/python/training/monitored_session.py", line 1091, in run
    return self._sess.run(*args, **kwargs)
  File "/anaconda3/lib/python3.7/site-packages/tensorflow/python/client/session.py", line 929, in run
    run_metadata_ptr)
  File "/anaconda3/lib/python3.7/site-packages/tensorflow/python/client/session.py", line 1152, in _run
    feed_dict_tensor, options, run_metadata)
  File "/anaconda3/lib/python3.7/site-packages/tensorflow/python/client/session.py", line 1328, in _do_run
    run_metadata)
  File "/anaconda3/lib/python3.7/site-packages/tensorflow/python/client/session.py", line 1348, in _do_call
    raise type(e)(node_def, op, message)
tensorflow.python.framework.errors_impl.InvalidArgumentError: assertion failed: [Unable to decode bytes as JPEG, PNG, GIF, or BMP]
	 [[{{node case/cond/cond_jpeg/decode_image/cond_jpeg/cond_png/cond_gif/Assert_1/Assert}}]]
	 [[node IteratorGetNext (defined at /anaconda3/lib/python3.7/site-packages/tensorflow_estimator/python/estimator/util.py:110) ]]
   ```
