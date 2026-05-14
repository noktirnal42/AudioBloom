# Third-Party Notices

AudioBloomAI is proprietary commercial software, but it uses or can interoperate
with the third-party components listed below. Those components remain under
their own licenses. This notice is provided for attribution and license
compliance; it does not change the AudioBloomAI commercial license.

## projectM / libprojectM

AudioBloomAI uses `libprojectM` for Milkdrop/projectM preset rendering.

- Upstream project: <https://github.com/projectM-visualizer/projectm>
- Version used by the current macOS runtime: projectM 3.1.12
- License: GNU Lesser General Public License, version 2.1
- License text: [licenses/LGPL-2.1.txt](licenses/LGPL-2.1.txt)
- Source release: <https://github.com/projectM-visualizer/projectm/releases/tag/v3.1.12>

AudioBloomAI links projectM as a shared library. The projectM library is not
subject to the AudioBloomAI commercial license; it remains available under the
LGPL-2.1. Users may replace or relink the projectM shared library as permitted
by the LGPL.

If you need the exact projectM source corresponding to an AudioBloomAI build,
use the upstream projectM 3.1.12 release above or contact support.

## Milkdrop / projectM Presets

AudioBloomAI can load Milkdrop/projectM preset files (`.milk`, `.prjm`) supplied
by the user or by compatible preset collections. Preset files are creative works
owned by their respective authors unless otherwise stated. AudioBloomAI preserves
preset filenames and visible author names where available.

Any preset pack bundled with or linked from AudioBloomAI should only include
files that are redistributable for that purpose. If you believe a preset has
been included or referenced incorrectly, contact support and it will be reviewed.

## Syphon Framework

AudioBloomAI uses Syphon for macOS frame sharing with compatible VJ and video
tools.

- Upstream project: <https://github.com/Syphon/Syphon-Framework>
- License: Syphon Framework BSD-style license
- License text: [licenses/SYPHON-LICENSE.txt](licenses/SYPHON-LICENSE.txt)

Syphon Framework License:

Copyright 2010 bangnoise (Tom Butterworth) & vade (Anton Marini).
All rights reserved.

Redistribution and use in source and binary forms, with or without modification,
are permitted provided that the conditions in
[licenses/SYPHON-LICENSE.txt](licenses/SYPHON-LICENSE.txt) are met.

## Apple Frameworks

AudioBloomAI uses Apple platform frameworks provided with macOS and Xcode for
native app functionality, audio capture, camera capture, rendering surfaces, and
system integration. Apple frameworks are subject to Apple's applicable software
licenses and developer agreements.
