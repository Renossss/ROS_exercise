# Create your own talking nodes

You need to create two nodes that will talk to each other via ROS2 topics.

Befor you start you need to know how to create a subscriber.

## Subscriber

Subscriber is very similar to publisher. We need to create the subscriber within `__init__` function.

```python
self.sub = self.create_subscription(String, 'chatter', self.callback_function, 10)  #create subscriber
```

but it recives a function name as a parametr and this function should parse a massage
```python
def callback_function(self, msg):                       # receive massage
    self.get_logger().info('I heard: "%s"' % msg.data)  # parce it
```


## Let's create our own nodes!

To do so, you have two directories, similar to the ones in the previous chapter.

Create a nodes that could talk to each other.

Ask for help if you need it.