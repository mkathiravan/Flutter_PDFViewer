# flutter_pdfviewer

 There are different packages which you can use to open a pdf in your app some are a bit complicated and some are easy to implement and here I am going to explain one of the easiest ways to use it.

Add the following dependencies on your pubspec.yaml file

  pdf_flutter: 
  
  file_picker: 
  
 # File from Asset Folder:
  From the asset folder, you can easily access your pdf file if you have mentioned it in your pubspec.yaml file. Here you are also required to mention placeholder in case of unavailability of resources.
  
       PDF.assets(
      "assets/demo.pdf",
      height: MediaQuery.of(context).size.height,
      width: MediaQuery.of(context).size.width,
      placeHolder: Image.asset("assets/images/pdf.png",
          height: 200, width: 100),
    ),
     
  
  # File from Phone Storage:
  Some times you need to access pdf from your phone especially in the case when you are posting any document in the server. The only thing which is different from the above code is PDF.file and but as we are picking it up from phone so we need to add the dependency of file_picker then we need to create an instance of the file picker
  
    File localFile;
        PDF.file(
      localFile,
      height: MediaQuery.of(context).size.height,
      width: MediaQuery.of(context).size.width,
      placeHolder: Image.asset(
        "assets/images/pdf.png",
    height: 200, width: 100
      ),
    ),
    
 # File from Server:
   Accessing pdf file is quite the same as the two mentioned methods you only need to use PDF.network and need to provide the link and this will show the pdf on your device.
   
        PDF.network(
      'https://google-developer-training.github.io/android-developer-fundamentals-course-concepts/en/android-developer-fundamentals-course-concepts-en.pdf',
      height: 300,
      width: 200,
      placeHolder: Image.asset("assets/images/pdf.png",
          height: 200, width: 100),
    ),
    
    
 ![image](https://user-images.githubusercontent.com/39657409/88256396-de221800-ccd8-11ea-9de5-a8d244cf247f.png)
   
