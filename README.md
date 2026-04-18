Overview
   
The Camera Chromaticity & Gamut Mapping Tool is a self-contained, single-file HTML application that visualises the colour gamuts of professional digital cameras and compares them against industry-standard target colour spaces. It requires no server, no installation, and no network connection — open the HTML file in any modern browser.
The tool is built on the CIE 1931 xy chromaticity diagram and presents two complementary plot types: a traditional CIE 1931 xy diagram and an xy polar plot centred on the working white point. Camera characteristics are derived from DNG ForwardMatrix 2 values extracted with ExifTool.

Key Capabilities

Plot native sensor gamuts as triangles on the CIE 1931 xy diagram and polar plot
Compare up to ten cameras simultaneously; multi-select up to two for detailed analysis
Visualise gamut mapping to six target colour spaces using four distinct strategies
Bradford chromatic adaptation between D50 and D65 working white points
Quantitative analysis: gamut area %, per-primary hue and chroma deltas
Natural-language comparative narrative for primary hue shift direction and magnitude

Technical Basis
Camera gamuts are defined by DNG ForwardMatrix 2 (FM2), which encodes the linear transform from balanced camera raw RGB to CIE XYZ under D65. Extracting the matrix columns yields the chromaticity coordinates of each primary. Chromatic adaptation uses the Bradford transform with ICC-standard matrix values, consistent with professional ICC colour management workflows.
A note on sub-locus primaries: modern camera sensors can produce primary chromaticities mathematically outside the spectral locus. These are valid virtual primaries — a property of sensor physics, not a data error.
