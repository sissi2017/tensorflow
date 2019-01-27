the loss function:
the minimal square error
the cross entropy
the personal define
MSE:tf.reduce_mean(tf.square(y_-y))

the backward propagation:
tf.train.GradientDescentOptimizer(0.001),minimize(loss_mse)
tf.train.AdmOptimizer()
tf.train.

tf.where()

ce = -tf.reduce_mean(y_*tf.log(tf.log(tf.clip_by_value(y,1e-12,1.0))))
softmax:

ce = tf.nn.sparse_softmax_cross_entropy_with_logits(logits = y,labels = tf.argmax(y_,1))
cem = tf.reduce_mean(ce)


learning rate:
学习率过大，会导致待优化的参数在最小值附近波动，不收敛;学习率过小，会导致待优化的参数收 敛缓慢。

learining_rate = LEARNING_RATE_BASE*LEARNING_RATE_DECAY*(global_step/LEARNING_RATE_BATCH_SIZE)
global_step = tf.Variable(0,trainable = Flase)
learning_rate = tf.train.exponential_decay(
LEARNING_RATE_STEP,LEARNINH_RATE_DECAY,
staircase = True/Flase)


