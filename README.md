# 935
Out of the four ways of serialization I was given to look at and compare, every option have it’s pros and cons. The four ways : JSON, MsgPack, pickle, and Protobuf are useful to a point and for different things.
# pickle
For starters pickle can serialize arbitrary Python objects, whereas JSON and MsgPAck have limits on the type of fate they can write out this mostly won’t be an issue for for our project. Pickel is out of the four the slowest and largest of the four, so what I recommend the least.
# JSON
So left with three I studied some tests between the them and their use with large data.  JSON has very widespread support and, debatably, the best alternative to XML, having a lightweight format it’s used for data interchanging. JSON has the largest size of the three and the longest serialization, yet is in the middle for deserialization. 
# MsgPack
MsgPack is described to be “like JSON. But fast and small.” it is more space efficient than JSON(being binary, more efficient storage of small integers), however it’s not the best choice for client-side serialization. In the test MsgPack returned the smallest size and shortest serialization, however it had the longest deserialization which was far greater than our other options. 
# Protobuf 
Protobuf is a binary encoded format that allows you to specify a schema for your data using a specification language and is more maintainable than the other options. Protobuf had the second smallest size from the tests and the second shortest serialization which is off by an extremely small fraction on the tests, plus it had the shortest deserialization
# Conclusion
After all the test I personally think that Protobuf is the best way to go. Not only does it have relatively small sizes it has a serialization that is the second shortest but is close enough to MsgPack’s serialization it doesn’t really matter. Not to mention that it has the shortest deserialization. 
