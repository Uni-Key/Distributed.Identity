# How BiometricUnlock() works and How your data is stored
Filesystems are composed of blocks, the smallest unit of addressable storage. Technically these are Logical blocks, as the physical can be remapped. They are an ordinal "numbered" Set.

# 1. Splitting up your Data
Your Personal Data Archive aka "Vault" (EternalFS) is a distributed Filesystem. This uses Erasure Coding to split it into Total/k parts. Each block is are encrypted with the same "Base Key"
Now we generate Parity blocks.
We take your Biometric values and assign each one to a Parity fragment! making a 1 to 1 Map & relationship! If you enter 1 Biometric into the network? It Encrypts the fragment with a unique Key which is stored on the network.

# 2. Biometrics values generate Keys! in a 1 to 1 mapping.
You can Retrieve Exactly 1 parity block for biometric that you put in. Want redudancy, in case of bodily injury "lost" biometrics? Each fingerprint is a separate
We use Biometrics to generate Encryption keys. Your original "Base Key" for the archive is stored alongside each "Parity Key". Meaning if you enter a single biometric? You can now Decrypt all the Public k-1 fragments stored on the Network.

# 3. Erasing 1 Public Fragment from the Network making your Archive irretrievable without you
Now: We Erase 1 of the k Parts! Therefore the Network only stores (k-1) fragments of the original data! This makes your Archive irretrievable, without additional Parity! It require atleast one parity block to recover the data!

# 3. Subvolumes & Additional Keys & Locks (Friends can help you Login)
You can lock down & re-encrypt subvolumes in your Vault as requiring Additional Biometrics, Multi-factor & Safeguards to unlock! This can be done by generating Additional Parity Keys from these inputs, And hiding more fragments from the network!
Additional Parity Keys like: a friend who helps you login, Or a UbiKey, can be created and set "Required" to recover the Subvolume!
**The difference with 3rd Party keys like a Friends's fingerprint Is those Fragments DO Not store your "Base Key"!** So your Friend Cannot decrypt your archive without you present! But by entering theirs they can help you Unlock yours by providing you additional Parity Fragments & keys!

# Use secure Computing to process Biometrics & Retrieve your data
We you go to a Kiosk or secure Uni.os phone? You can now input your Biometrics and retrieve your Parity keys. You can also have your Friends or trusted
This also unlocks your ID allowing you to find the Network location of every block of your EternalFS!

1. Uni-Key uses 
2. We then add n parity bits on top!
Each part is Encrypted Separately using own key! It is a cycle, that starts 

Each Biometric value is mapped to 1 Encryption key and when you Use it to Login? You are able to retrieve from the network the Final Key required to Decrypt your Vault!

# Fundamentals
https://en.wikipedia.org/wiki/Erasure_code
https://en.wikipedia.org/wiki/Mojette_Transform
>Erasure coding ransforms a message of k symbols into a longer message (code word) with n symbols such that the original message can be recovered from a subset of the n symbols. The fraction r = k/n is called the code rate. The fraction k’/k, where k’ denotes the number of symbols required for recovery, is called reception efficiency.
