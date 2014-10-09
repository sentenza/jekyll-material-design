---
layout: post
category : lessons
tagline: "Supporting tagline"
tags : [jekyll, code]
---
{% include JB/setup %}

An example post about code insertion into posts.

<!--more-->
## Testing code snippet highlight

The following example shows how to highlight a piece of code throughout the use of pygments:

{% highlight python %}
class Singleton(type):
    """Base metaclass for Singleton pattern
@see http://stackoverflow.com/a/6798042/1977778
"""
    _instances = {}
    def __call__(cls, *args, **kwargs):
        if cls not in cls._instances:
            cls._instances[cls] = super(Singleton, cls).__call__(*args, **kwargs)
        # If you want to run __init__ every time the class is called, add the following else condition
        # else:
        # cls._instances[cls].__init__(*args, **kwargs)
        return cls._instances[cls]
{% endhighlight %}

## Code highlighting with redcarpet

Another snippet rendered with the most common Github code syntax:


``` python
    def strip_nonascii(self, s):
        """This method remove non-ascii chars from argument"""
        return ud.normalize('NFKD', unicode(s) ).encode('ascii','ignore')


    @db_commit
    def create_users_table(self, cursor):

        """ Check the existence of the users log table, otherwise create it """

        pass
```

``` scala

package astrac.akka.askretry

import akka.actor._
import akka.util.Timeout
import akka.pattern.ask
import scala.concurrent.duration._
import scala.concurrent.Future

object RetryingActor {
  case class Ask[T](target: ActorRef, message: T, rate: FiniteDuration,
  maxAttempts: Int)
    case object Retry
    
      case class RetryException(attempts: Int) extends Exception(s"Cannot retry
      after $attempts attempts")
      
        def props[T] = Props[RetryingActor]
        }
```

**Check the markdown of this example in order to fully comprehend the correct syntax.**

[Here](https://github.com/sentenza/sentenza.github.io/issues/1) you can find more detailed information.
