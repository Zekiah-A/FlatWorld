# Technical specifications
 - Blocks are represented by two 6bytes, `Block type` and `Height`
 - The world is made up of 255 layers, with only the top layer (as visible from a bird's eye view)
 - The world is split up into 16x16 pixel chunks so we can keep the data transmission reasonable
 - Tiles like water are exceptions, which are able to flow on top of lower layers
 - Chunks are a map of `String(x + y (stringwise), i.e (5, 5) -> 55) : Uint8Array(255*16*16=65536)`