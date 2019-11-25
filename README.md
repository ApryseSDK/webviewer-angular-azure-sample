# Angular Azure PDF Viewer Sample (WebViewer)

[WebViewer](https://www.pdftron.com/webviewer) is a powerful JavaScript-based PDF Library that's part of the [PDFTron PDF SDK](https://www.pdftron.com). It provides a slick out-of-the-box responsive UI that interacts with the core library to view, annotate and manipulate PDFs that can be embedded into any web project.

![WebViewer UI](https://github.com/PDFTron/webviewer-angular-azure-sample/raw/master/sample.png)

This repo is specifically designed for any users interested in integrating WebViewer into an Angular Azure project. This project can be viewed from [azurewebsites.net](https://myfirstazurewebapp20191113124838.azurewebsites.net/webviewer).

## Initial setup

Before you begin, make sure your development environment includes [.NET Core 3.0 SDK](https://dotnet.microsoft.com/download/dotnet-core/3.0) and [Node.js](https://nodejs.org/en/).

## Install

```
git clone https://github.com/PDFTron/webviewer-angular-azure-sample.git
cd webviewer-angular-azure-sample
npm install
```

## Run

```
npm start
```

Navigate to `https://localhost:9001/webviewer`

## WebViewer APIs

See [API documentation](https://www.pdftron.com/documentation/web/guides/ui/apis).

## Enabling full API

PDFNetJS Full is a complete browser side PDF SDK, unlocking viewing, parsing and editing of PDF files. To enable full API, you can modify constructor in `wwwroot/js/webviewerScripts.js`:

```diff
initWebViewer: function () {
    const viewerElement = document.getElementById('viewer');
    WebViewer({
        path: 'lib',
        initialDoc: 'https://pdftron.s3.amazonaws.com/downloads/pl/demo-annotated.pdf', // replace with your own PDF file
+        fullAPI: true
    }, viewerElement).then((instance) => {
        // call APIs here
    })
}
```

You can refer to this [guide for more information](https://www.pdftron.com/documentation/web/guides/pdfnetjsfull-getting-started)

## License

See [license](./LICENSE).
