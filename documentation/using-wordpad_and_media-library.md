# kravspec på media-bibliotek
1. Hämtar  bild via URL
2. Hämtar bild, Går det att hämta metadatan ? 
3. Bulkuppladda ?
4. Skapa en användare som bara kan lägga till bilder ?
5. Hur fungerar REST API i plug-in Enhanced Media Library ? 
6. Kan man lägga till extra fält, metadata(key/value) , såsom ex 'Licens-type' 

## kravspec på Wordpress (ex. fjärilslistan) 
1. kunna ladda upp excel-filer
2. kunna ladda upp pdf etc
3. Skapa en användare som bara kan lunderhålla 1 lista med ...

### wordpress, vad finns
- 'Lägg till användare'
Följande roller finns
1. prenumerant
2. bidragsgivare
3. författare
4. redaktör
5. Administratör

- **Q: finns det möjlighet att ha en 'bildredaktör' ?**

Uppladdning av bilder -> 'Maximal filstorlek för uppladdning: 2 MB.  '

# orginal installation, utan tillägg

Möjligt att skala bilder etc.

## Ladda upp bilder
- laddar upp en bild 
- kan hämta bild , kopiera URL , http://localhost:8080/wp-content/uploads/2021/09/tv-test-pattern-146649_960_720.png 
- går det att förenkla denna URl?
- **Q: Hämtar bara bild, men inte metadata ... ?** Går det att hämta metadatan ?

### hur integrerar man detta exempelvis med naturforskaren?
- ladda upp
- hämta

### wordpress[enhanced Media Library] borde passa Tobias och Zoologi/Entomologi, spara och hämta bilder
- ladda upp bilder
- hämta bilder via url
- skapa en hiearki, Zoology/entomology etc (se Enhanced Media Library)

-> https://wpuxsolutions.com/support/create-new-ticket 


### wordpress [som det är] borde passa Tobias och fjärilslistor ?
Se exempelvis denna checklista -> https://euphrasia.nu/ 



# med 'media library'-tillägg.
- vilket passar bäst
- kan man ge en wordpress-användare enbart tillgång att lägga upp bilder ?

## testar.
https://sv.wordpress.org/plugins/media-library-plus/

-> Using Media Library Folders for WordPress 
```
To get started download and install the Media Library Folders for WordPress plugin. 
Once Media Library Folders for WordPress is activated you will see Media Library Folders for WordPress in the WordPress dashboard menu. 
And you are ready to go watch our super helpful intro video!
```

### 'populärt tillägg' - WordPress Gallery Plugin

NextGEN Gallery has been the industry’s standard WordPress gallery plugin since 2007 and continues to receive over 1.5 million new downloads per year. It’s easy for simple photo galleries, but powerful enough for the most demanding photographers, visual artists, and imaging professionals.

## testar
https://wordpress.org/plugins/search/media+library/ 

### filebird -> 100,000+ active installations  
https://wordpress.org/plugins/filebird/ 
- Free and Pro

```
FileBird enhances your media library with clean UI, native icons, smooth drag & drop, advanced sort and organization.
```

### media-library-assistant -> 70,000+ active installations 
https://wordpress.org/plugins/media-library-assistant/ 

----------------------------------------------------------------------

----------------------------------------------------------------------

### Enhanced Media Library -> 100,000+ active installations 
https://wordpress.org/plugins/enhanced-media-library/
- Free and Pro

1. Loggar in på wordpress.org och markera det som 'favorit'
2. egen wordpress, 'lägg till tillägg' -> http://localhost:8080/wp-admin/plugin-install.php?tab=favorites 
3. tryck på 'hämta favoriter'
4. tryck på 'installera'
5. tryck på 'aktivera'

```
Developer-Friendly

    Core hooks just work for media taxonomies and media items
    All taxonomies supported: custom and code-registered
    REST API supported out of the box
    No custom tables in the database
    Deactivation makes no harm to data: all media items and taxonomies remain after deactivation

```

#### MIME Types Management

Add or remove file types, allow or disallow uploading.
The plugin incorporates a file type into media filters if you wish. 

#### pro
- bulk edit ( vad betyder det ?)
- sökning i 'titles'/'captions'/'descriptions'/'authors' etc

https://wpuxsolutions.com/plugins/enhanced-media-library-pro
