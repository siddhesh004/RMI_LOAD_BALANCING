# RMI_LOAD_BALANCING

The universal service browser that we can observe is like a specialized web browser, except instead of HTML pages, the service browser downloads and displays interactive Java GUIs that we're calling universal services.

Remote Method Invocation (RMI) is an API which allows an object to invoke a method on an object that exists in another address space, which could be on the same machine or on a remote machine. Through RMI, object running in a JVM present on a computer (Client side) can invoke methods on an object present in another JVM (Server side). RMI creates a public remote server object that enables client and server side communications through simple method calls on the server object.

The communication between client and server is handled by using two intermediate objects: Stub object (on client side) and Skeleton object (on server side).

We have 3 services (mini-applications) in InterfacesForRMIBrowser.java, which are called DiceService, MiniMusicService and DayOfTheWeekService respectively.

Each one has its own class.

But we also have interface Service. This is the key to everything. This very simple interface has just one method, getGuiPanel(). Every service that gets shipped over to the client must implement this interface. This is what makes the whole thing UNIVERSAL.
