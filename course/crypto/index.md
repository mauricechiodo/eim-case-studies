---
Title: Cryptography and Government Surveillance
Template: ListSubPages
GridImage: http://cueimps.soc.srcf.net/course/media/lock1.png
---

The right to privacy is protected by the European Court of Human Rights. In the Bill of Rights, Madison's concern over the protection of privacy is reflected. In almost every country in the world there exists some legal protection of a citizen's privacy. Therefore, when transmitting data across the internet - basically an open channel - it has always been of great concern that we be able to protect what it is that we are sending. When I started editing this website, I had to go to GitHub and put in my login information. If the data I sent wasn't protected, any adversary would be able to take that and read my private files, or use it against me. The same goes for emails, Facebook, Cloud files and more. The world is becoming more and more digital and protections need to exist to protect privacy.

Cryptography is the method by which this is achieved, a branch of number theory. The current most common form of cryptography requires a shared secret to be generated accross a public platform, thus allowing shared knowledge of how to decrypt messages sent. Currently, this relies on [Diffie-Hellman key exchange](course/crypto/diffiehellman) that uses group theory and the idea that the discrete logarithm problem is difficult to crack.

Many agents have a vested interest in being able to read encrypted internet traffic, be these government intellegence agencies like the NSA or terror units that have an interest in using the internet and private files to spread a message. It has been [hypothesised](course/crypto/nfs) that commonly used parameters in the key exchanges preceding encrypted communications may permit a sufficiently motivated and resourced attacker to decipher communications in real time.

Mathematicians are working every day on making the internet more secure, or on breaking that security. Regardless of who should be able to read internet traffic, or if one deserves online privacy, these are poignant ethical questions that mathematicians are being faced with all the time.

Link to introduction on [ECC and NIST](https://cueimps.soc.srcf.net/course/course/crypto/Nist) - it contains links to the more detailed ECC and NIST pages.
