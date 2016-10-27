# Mock EPUB3 Toolchain

An example toolchain with video, text and assessment content. To build, you'll need pandoc installed.

## Example

```
pandoc -s -t epub3 -o product.epub src/*.md data/metadata.yaml --toc --template=data/default.html
```

Outputs an EPUB3 from MD, using a custom EPUB3 template (that includes Packt rights notices).
