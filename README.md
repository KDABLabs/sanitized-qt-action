# sanitized-qt-action

A GitHub Action which installs a Qt built with sanitizer support.

Used internally by KDAB for the open-source KD* products CI. Only 6.11 LGPL Qt is supported.

## Example

```yaml
    - name: Setup Sanitized Qt
      uses: ./
      with:
         release: "6.11"
         qt-version: "v6.11.0"
         qt-flavor: asan
```

## release

Only accepts "6.11" currently.

## qt-version

Can be a sha1, a version tag or anything associated with the release.
Only "v6.11.0" supported currently.

## qt-flavor

This accepts `asan`, `tsan`, `debug` or `profile`. `asan` includes `lsan`.
All of them, even `profile` have asserts enabled and are.

## Warning

Use for CI purposes only, as all binaries are Qt developer builds, not suitable for production.

## License

The sanitized-qt-action Software is © Klarälvdalens Datakonsult AB (KDAB), and is
available under the terms of the [MIT](LICENSES/MIT.txt) license.


## About KDAB

sanitized-qt-action is supported and maintained by Klarälvdalens Datakonsult AB (KDAB).

The [KDAB](https://www.kdab.com) Group is a globally recognized provider for software consulting,
development and training, specializing in embedded devices and complex cross-platform desktop
applications. In addition to being leading experts in Qt, C++ and 3D technologies for over
two decades, KDAB provides deep expertise across the stack, including Linux, Rust and modern UI
frameworks. With 100+ employees from 20 countries and offices in Sweden, Germany, USA, France
and UK, KDAB serves clients around the world.

Please visit [the KDAB website](https://www.kdab.com) to meet the people who write code like this.

[Blogs and publications](https://www.kdab.com/resources)

[Videos (Tutorials and more)](https://www.youtube.com/@KDABtv)

[Software Developer Training for Qt, Modern C++, Rust, OpenGL and more](https://training.kdab.com)

[Software Consulting and Development Services for Embedded and Desktop Applications](https://www.kdab.com/services/)
