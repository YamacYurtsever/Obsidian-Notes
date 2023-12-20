- *Bit*: Smallest representation of data in a computer, can be 0 and 1 ^f57512
- *Byte*: 8 bits, can be 256 different values ^ff39e6
- *Binary*: Base 2 number system (0, 1) ^79c0a2
- *Decimal*: Base 10 number system (0, 1, 2, 3, 4, 5, 6, 7, 8, 9) ^b773f4
- *Hexadecimal*: Base 16 number system (0, 1, 2, 3, 4, 5, 6, 7, 8, 9, A, B, C, D, E, F)
! The prefix "0x" is used to indicate that a value is written in hexadecimal ^94fc55

#### Conversion Between Number Systems
![[Number System Conversion.png | 450]]

#### Memory Sizes of Variables
- **char** -> 1 [[#^ff39e6 | byte]]
- **int** -> 4 byte
- **long** -> 8 byte
- **float** -> 4 byte
- **double** -> 8 byte
- **string** -> n. of chars + 1 (terminating null)
- **pointer** -> 8 bytes ([[CPU#^349764 | 64-bit systems]])

#### Representing Real World Data (Analog Data vs Digital Data)

| Analog Data                           | Digital Data                          |
| ------------------------------------- | ------------------------------------- |
| Infinite                              | Finite                                |
| Continuous                            | Discrete                              |
| Representative of the real world      | Usable by computers                   |
| Easier to store, maintain and analyze | Harder to store, maintain and analyze |
| E.g.: Spectrum of colors on a rainbow | E.g.: It's image on a computer        | 

- The [[Operating System#^ff1db3 | drivers]] on the operating system converts the analog data that comes from the input
device into digital data that the computer can use

#### Representing Textual Data
- Binary data is used to represent textual data through characters sets such as ASCII and Unicode where binary values correspond to characters
- ASCII: An encoding standard used to represent characters in the english alphabet as binary values, it originally used 7 bits to represent each character thus there are 128 possibilities
- Unicode: A newer encoding standard used to represent characters from all common languages, emojis and symbols as binary values, UTF-32 uses 4 bytes to represent each character thus there are about 4 billion possibilities
- The ASCII representation for  'A' is 65 and every letter is 32 away from its lowercase or uppercase equivalent, so the code for 'a' is 97.

![[ASCII Table.png]]

#### Representing Audio Data
- After going through the microphone, audio data gets converted into binary and is
represented as discrete numeric values
- The time between each capture of the audio is called sampling rate, the less the time is
between each capturing of the audio, the higher the sampling rate will be and the higher the quality of the recording will be
- After a point the human ear won't be able to differentiate between sampling rates so it
becomes a good representation of reality
- Audio can be stored as MP3, MP4 or WAV

#### Representing Color Data
- Color is represented as **RGB** (Red, Green, Blue) values
- **Color depth** is the number of values each color can get
- In TrueColor, which is used by most modern computers, each value is between 0 and 255 (3 bytes)

#### Representing Images
- A digitized photograph is represented as a collection of pixels
- The amount of pixels in an image is called the resolution
- GIF, PNG, JPEG
- Vector art is a way of representing images in terms of lines and geometric shapes (good for
line art and cartoon style drawings)

#### Representing Videos
- Video clips consist of a sequence of  images
- Video codecs (compressor / decompressor) are tools for reducing the size of a video
- Video codecs use lossy compression to reduce the size of a video, therefore the aim is to lose data that is the least recognizable to the viewer