<h1>blipaudio</h1>

<h4 align="center"> Simple, easy audio in C/C++. </h4>

Features
=======
- Easy to build -- no dependencies except the Standard Library.
- High and low-level API -- you can get control over every buffer you write!
- (*) Decoding for WAV, FLAC, MP3, and pass in your own!
- (*) Encoding for WAV, FLAC
- Manage sound files you've already made

Examples
========
Play back a sound using the high-level API.
``` c
#include "blipaudio/blipaudio.h"
#include <stdio.h>

int main(void) {
  // Create a context, which holds everything about the instance of blipaudio currently invoked.
  unsigned int context;
  // Then make a context with the unsigned int as the context ID.
  bp_make_context(&context);

  if (BP_HAS_ERROR != N) {
  // Just check for errors.
    return -1;
  }

  // Now we play sound!
  bp_play(&context, "path/to/sound/file.wav");
  printf("Quit with the ENTER key.\n");
  getchar();
  return 0;
}
```
