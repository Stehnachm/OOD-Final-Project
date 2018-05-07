# Implementation of listeners and event handlers

## Swift
In Swift, Events provide a generic mechanism for raising notifications that can be handled by multiple observers. The Event class has a generic parameter T which defines the type of data that this event conveys and the EventHandler typealias declares a function that accepts this type. The rest of this class is pretty straightforward, handlers are added to an array, with each being invoked when the event is raised. In the code, after the declaration of the Event Class, we create an event and add a handler to the eventHandler list. We then can pass multiple parameters to event handlers via tuples.

- Documentations:
    > In Swift, it use eventing mechanism to implement event handling.
    > Events provide a generic mechanism for raising notifications that can be handled by multiple observers.
```
public class Event<T> {
public typealias EventHandler = T -> ()
private var eventHandlers = [Invocable]()
public func raise(data: T) {
    for handler in self.eventHandlers {
        handler.invoke(data)
            }
        }
public func addHandler<U: AnyObject>(target: U,
    handler: (U) -> EventHandler) -> Disposable {
        let wrapper = EventHandlerWrapper(target: target,
        handler: handler, event: self)
        eventHandlers.append(wrapper)
        return wrapper
            }
        }
private protocol Invocable: class {
    func invoke(data: Any)
    }
 ```


## Java
* In Java there are a multitude of listeners and event handlers. An event handler can be placed onto just about any UI object to allow for mouseClick events and such. Listeners can be placed on all sorts of properties, and you can even create your own properties to be listened to. 
```java
server.addEventListener("message", clientData.class, new DataListener<clientData>() {
        @Override
        public void onData(SocketIOClient client, clientData data, AckRequest ackRequest) throws Exception {
            System.out.println("Message from client: " + data.getMessage());

        }

    });
```

*example, the MouseListener. An EventListener is an object that implements an interface for event handling.

```java
public class MyClass
{
    Button myButton;

    MyClass()
    {
        ...
        myButton.addMouseListener(new ButtonHandler());
    }

    public class ButtonHandler implements MouseListener
    {
        public void mousePressed(MouseEvent e) {}
        public void mouseReleased(MouseEvent e) {}
        public void mouseEntered(MouseEvent e) {}
        public void mouseExited(MouseEvent e) {}

        public void mouseClicked(MouseEvent e)
        {
           doSomething("Mouse clicked", e);
        }
    }
}
```

