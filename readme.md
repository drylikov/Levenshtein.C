




# Levenshtein(3)








Vladimir Levenshtein’s edit distance algorithm<sup>[1][wiki]</sup> as a C library. There’s also a CLI: [levenshtein(1)][cli], and a [JavaScript version][js].





## Installation





[CLib][]:

```sh
$ clib install drylikov/levenshtein.C
```

Or clone the repo.





## Usage





### `size_t levenshtein(const char *a, const char *b);`





```c
#include <stdio.h>
#include "levenshtein.h"

int
main(int argc, char **argv) {
  char *a = argv[1];
  char *b = argv[2];

  if (argc < 3) {
    fprintf(stderr, "\033[31mLevenshtein expects two arguments\033[0m\n");

    return 1;
  }

  printf("%zu\n", levenshtein(a, b));
}
```





### `size_t levenshtein_n(const char *a, const size_t length, const char *b, const size_t bLength);`


``` c
#include <stdio.h>
#include "levenshtein.h"

int
main() {
  const char *a = "foobar";
  const char *b = "hello";

  printf("%zu\n", levenshtein_n(a, 6, b, 5));
}
```

## License

[build-badge]: https://img.shields.io/travis/drylikov/levenshtein.c.svg

[build]: https://travis-ci.org/drylikov/levenshtein.c

[coverage-badge]: https://img.shields.io/coveralls/drylikov/levenshtein.c.svg

[coverage]: https://coveralls.io/github/drylikov/levenshtein.c

[wiki]: https://en.wikipedia.org/wiki/Levenshtein_distance

[cli]: https://github.com/drylikov/levenshtein

[js]: https://github.com/words/levenshtein-edit-distance

[clib]: https://github.com/clibs/clib




