# Ignore this specific import

> import cv2 # pylint: ignore=import-error

# Module [...] has no [...] member

This pytorch code will generate this error:

> x = torch.empty(2, 2) # Module torch has no empty member

It happens because inside torch, the empty function is actually
known by a different name, like: `torch._C.empty`

The workaround is to tell pylint to ignore this kind of error
from torch. Open `.pylintrc` and add:

> [TYPECHECK]
> # List of members which are set dynamically and missed by pylint inference
> # system, and so shouldn't trigger E1101 when accessed. Python regular
> # expressions are accepted.
> generated-members=numpy.*,torch.*
