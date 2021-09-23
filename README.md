# PdfSharp.HtmlToPdf
A .Net library that utilize PDFSharpCore to generate PDF file from HTML snippet.

The project uses opened source from https://archive.codeplex.com/?p=htmlrenderer. Deeply appreciate to original author.

# Usage

```cs

using DotNetBrightener.PdfSharp.HtmlToPdf;

// omitted code

var renderContent = $"{some-html-snippet}";

PdfGenerateConfig config = new PdfGenerateConfig();
config.PageSize		     = PageSize.A4;
// or use this 
// config.PageSize       = PageSize.Undefined; // PageSize.Undefined will resize the size of output page to the actual size of the content, useful for generating invoices / receipts to be printed with rolled papers in thermal printers
// config.ManualPageSize = new XSize(140, 1800); // sample 58mm thermal printer size.

config.SetMargins(0);

var doc = PdfGenerator.GeneratePdf(renderedContent, config);

var stream = new MemoryStream();
doc.Save(stream);

// or 
// var filePath = $"{path-to-file}.pdf";
// doc.Save(filePath);

```

# Reference

The project uses opened source from https://archive.codeplex.com/?p=htmlrenderer. Deeply appreciate to original author.

# License 
MIT License

Copyright (c) 2021 DotNet Brightener

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.


# Original Author Copyright And License Notice

Copyright (c) 2009, José Manuel Menéndez Poo

Copyright (c) 2013, Arthur Teplitzki

All rights reserved.

Redistribution and use in source and binary forms, with or without modification,
are permitted provided that the following conditions are met:

Redistributions of source code must retain the above copyright notice, this
list of conditions and the following disclaimer.

Redistributions in binary form must reproduce the above copyright notice, this
list of conditions and the following disclaimer in the documentation and/or
other materials provided with the distribution.

Neither the name of the menendezpoo.com, ArthurHub nor the names of its
contributors may be used to endorse or promote products derived from
this software without specific prior written permission.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND
ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED
WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE
DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE FOR
ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES
(INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES;
LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON
ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT
(INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS
SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.