# Third-party software

This application bundles dynamically linked, unmodified Qt/PySide libraries. Their license texts and the other bundled dependency notices are in `licenses` within the application resources (`Contents/Resources` on macOS, `_internal` on Windows). You may replace the Qt libraries with ABI-compatible modified builds. Nothing in FoldDeck's distribution restricts reverse engineering for debugging modifications to the LGPL components.

- Qt / PySide6 Essentials / shiboken6 6.12.0: LGPL-3.0, GPL alternatives, and third-party notices. [Qt source archives](https://download.qt.io/archive/qt/6.12/) · [PySide source](https://code.qt.io/cgit/pyside/pyside-setup.git/?h=v6.12.0) · [Qt licensing](https://doc.qt.io/qt-6/licensing.html).
- cryptography 50.0.2: Apache-2.0 or BSD-3-Clause; bundled OpenSSL has its own notices. [Source](https://github.com/pyca/cryptography/tree/50.0.2).
- qrcode 8.2: BSD. [Source](https://github.com/lincolnloop/python-qrcode/tree/v8.2).
- Python 3.12.16 (macOS build) / 3.14.10 (CI build): PSF License Agreement. [Source and license](https://www.python.org/downloads/source/).
- OpenSSL 3.5.9 LTS (macOS TLS runtime): Apache-2.0. [Source and releases](https://www.openssl-library.org/source/).
- cffi / pycparser: MIT/BSD license texts included in the distribution.
- PyInstaller 6.22.3: GPL-2.0 with bootloader exception permitting application distribution. [License](https://pyinstaller.org/en/stable/license.html).

Public releases must retain these notices and include the matching qtbase, qtsvg, qtimageformats and pyside-setup 6.12.0 source archives next to the application downloads. The pyside-setup archive includes shiboken. `packaging/collect_sources.py` obtains the unmodified archives and verifies Qt's published SHA-256 checksums. Packaging is intentionally directory based rather than a self-extracting single executable to preserve access to the shared libraries.
