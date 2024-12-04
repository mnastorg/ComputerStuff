# Understanding Memory Storage in Machine Learning

## Bits and Bytes

A **Bit** (binary digit) is the smallest information unit : it is 0 or 1. A bit is the smallest container in which a set of information can be stocked. Bits are not used to represent storage capacities.

A **Byte** is the smallest quantity of data and define a memory unit. It is also called *octet* inf french. Bytes are used because computers can only process a small amount of bits for data transmission and storage. 

**1 Byte = 8bits**. A Byte can thus represent 2^8 different states. 

If you think of a bit as a binary letter, then a Byte is the smallest binary word that can be formed from it. To represent actual letters or alphanumeric characters, at least one Byte is needed.

As a unit of measurement, the Byte is too small to represent large amounts of data. Therefore, powers of magnitude are used. There are two standards for denoting multiples of Bytes: binary prefixes and decimal prefixes.

In the decimal prefix system, powers of 10 are used with symbols like K, M, G, T, etc. For example:
- 1 KB (Kilobyte) = 1,000 Bytes
- 1 MB (Megabyte) = 1,000,000 Bytes
- 1 GB (Gigabyte) = 1,000,000,000 Bytes

In the binary prefix system, powers of 1024 are used with symbols like Ki, Mi, Gi, Ti. For example:
- 1 KiB (Kibibyte) = 1,024 Bytes
- 1 MiB (Mebibyte) = 1,048,576 Bytes
- 1 GiB (Gibibyte) = 1,073,741,824 Bytes

These binary prefixes are often mistakenly confused with the decimal ones (e.g., G for Gigabyte and Gi for Gibibyte), which can lead to misunderstandings in data size and capacity. However the error is small.

*Conclusion:* Bits are used as a unit of measurement to describe the speed and amount of data consumed, typically represented by the data transfer rate. They indicate how many units of data are transferred within a given period of time. Bytes, on the other hand, serve as a unit of measurement for data quantities, defining storage capacity and possible data sizes.

## Memory Requirements for Deep Learning Models

Let's take the Mistral 7B model as an example to understand the memory requirements for inference, fine-tuning, and training.

### Background

As explained earlier, the basic unit of memory is the byte, and larger units are based on powers of 1024. For example:
- 1 KB = 1,024 Bytes
- 1 MB = 1,024 KB
- 1 GB = 1,024 MB

For the Mistral 7B model, "7B" indicates the model has 7 billion parameters. Common data types for parameters include:
- **float**: 32-bit floating point, 4 bytes (**single precision**)
- **half/BF16**: 16-bit floating point, 2 bytes (**half precision**)
- **int8**: 8-bit integer, 1 byte
- **int4**: 4-bit integer, 0.5 byte

### Estimating Memory Usage for Inference

For the Mistral 7B model using BF16, the memory requirement can be calculated as:
- 7 billion parameters * 2 bytes = 14 billion bytes = 14 GB (approx. using (1000/1024)^3 ~ 0.93)

For simplicity, we often assume the ratio as 1, so the Mistral 7B model with BF16 would require approximately **14 GB** of memory for inference. It’s wise to slightly overestimate as additional memory beyond the parameters might be needed.

For comparison, the memory usage for a LLaMA2-13B model can be estimated as:
- **Float**: 13 billion parameters * 4 bytes = 52 GB
- **Half/BF16**: 13 billion parameters * 2 bytes = 26 GB

### Estimating Memory Usage for Training

During training, integer-based parameter types like **int8** and **int4** are not sufficient for ensuring model convergence. Typically, **float** is used, though **BF16** can be an option for slightly lower precision and memory usage.

Training generally requires 3 to 4 times more memory than inference due to back-propagation, optimization algorithms (like Adam), and the transformer architecture. A safe estimate is to use a factor of 4.

For instance, the estimated memory required for training the Qwen-7B model is:
- **Float**: 7 billion parameters * 4 bytes * 4 = 112 GB
- **Half/BF16**: 7 billion parameters * 2 bytes * 4 = 56 GB
