# eager-malloc

LD_PRELOAD malloc wrapper that forces page faults of every allocated
byte, to ensure that memory allocation time as accounted for in
profiles. Without touching or force-faulting fresh memory, these costs
can get `smeared' over subsequent code that uses the memory.
