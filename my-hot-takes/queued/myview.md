# VPS are pointless as "anti-censorship" tools

(Transcription - expect some errors)

I have a couple of friends who are really into privacy and very adverse to the idea of government censorship, et cetera. These folks are very much into using VPN's wherever possible. 

This exposition of my viewpoint is a summary of the main points I would argue if one of those friends were in front of me right now and ask me why I (mostly) don't use a VPN. 

VPNS are useful when you are using a untrusted connection and you are concerned that the network may be unsecure (MITM), subject to phishing etc. I try to always use a VPN whenever I'm in a hotel, etc, although we have good cellular where I live so it's not an everyday need.

I've thought about the idea of using an always on VPN connection at home since deploying OPNSense and seeing that it's actually fairly feasible to do so. My main hesitation to do so was that it would introduce unecessary latency and connection overhead, be arduous to set up - as well as the concern that it might actually complicate authentication because I couldn't rely on IP based auth.

I understand that VPNS and other forms of secure networks like Tor have use cases, especially in places with repressive regimes -  for example, where dissidents or journalists are very concerned about their communications being surveilled. This, however, is not the type of everyday use case that I am envisioning. But I would argue that some of my arguments may even hold some water in that case too. 

Here are my main lines of contetion:

The Internet is a connected network of nodes. If you wish to connect to the outside world, then you have to introduce vulnerability at some part of the chain. For example, Even if two parties are using end to end encryption The communication has to be decrypted at some point for the message to be intelligible to the other user. Perhaps a one time pad is an exception. But considering more routine forms of encryption, like GPG, there is a possibility that the recipient's computer might be compromised or subject to screenshotting or othre threats that may try to capture the text while in plain text and visible on a display.

An ordinary consumer who relies upon ISP connectivity to connect to the Internet is placing their trust in their ISP. Their ISP, however, is regulated by their government communication provider. It's reasonable to expect that a large volume of Internet traffic May make its way into signals intelligence pipelines. But also that An extremely small scope of this collection comes under human investigation. 

While some may find this process intrusive, it serves a greater good. Were consumer accessible encryption to be totally unbreakable then, by extension, it would mean that any bad actor would enjoy the absolute right to privacy. Instead, to thwart things like the coordination of crime, society agrees that some restriction upon this otherwise total privacy serves the greater good and is authorized by the legal authorities. 

The market for VPN providers is marked by a very low degree of transparency. Any VPN provider can make marketing claims such as keeping zero logs. However, it has always seemed to me that ultimately the user has to place their trust in this unknown VPN company. If the traffic has to be decrypted at the VPN provider's node and the VPN provider itself is a weak point in the system. 

This strikes me as very problematic. I would rather put my trust in a government that I know to be held to some kind of legal authority and have verifiable organization than to displace that trust and put it instead into a VPN provider. If we accept the point that VPN providers should and must be subject to some kind of legal enforcement mechanism because otherwise they could be used to facilitate crime, then it begs the question, what has been achieved by using them versus just using the Internet conventionally?

Finally - a tangential: I've often thought that if a government or a signals intelligence body were trying to make the job of finding potentially suspicious Internet activity easier and prosecute online crime That one of their most no brainer moves would be to set up front VPN companies or TOR exit nodes. If I'm not mistaken, this has in fact happened. This is one more one more reason Why? I feel that using these services in an attempt to evade perceived government surveillance is a self defeating strategy. 
