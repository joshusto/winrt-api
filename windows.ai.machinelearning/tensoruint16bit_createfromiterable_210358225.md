---
-api-id: M:Windows.AI.MachineLearning.TensorUInt16Bit.CreateFromIterable(Windows.Foundation.Collections.IIterable{System.Int64},Windows.Foundation.Collections.IIterable{System.UInt16})
-api-type: winrt method
---

<!-- Method syntax.
public TensorUInt16Bit TensorUInt16Bit.CreateFromIterable(IIterable<Int64> shape, IIterable<UInt16> data)
-->

# Windows.AI.MachineLearning.TensorUInt16Bit.CreateFromIterable

## -description
Creates a 16-bit unsigned integer tensor object, allocates a buffer of size *shape*, and copies all of *data* into it.

## -parameters
### -param shape
The size of the buffer.

### -param data
The data to copy into the buffer.

## -returns
A 16-bit unsigned integer tensor object with a buffer containing the given data.

## -remarks

### Thread safety
This API is thread-safe.

## -see-also

## -examples
