
N.B - A note about ***the `Active` switch***:

  Many sections of the Manifest have an `Active` switch.

  1) If the section is PRESENT and the switch is TRUE, the section is ACTIVE
  2) If the section is PRESENT and the switch is ABSENT, the section is ACTIVE (this should rarely happen)

  3) If the section is PRESENT and the switch is FALSE, the section is INACTIVE
  4) If the *section* is ABSENT, the section is INACTIVE

```
{
  "Page_Editorial": {

    "Main_Heading": "Scotia Beauty - Private Label Nail Products",

    "Byline" : {

      "Active" : false,
      "Name" : "",
      "Description" : ""
    },

    "Dateline" : {

      "Active" : false,
      "Location" : {"City" : "", "Region" : "", "Country" : ""},
      "Source": "",
      "DateTime" : ""
    },

    "Standfirst": {

      "Active" : false,
      "Copy" : ""
    }
  },


  "Meta_Information": {
  
    "Web" : {
    
      "Title": "Scotia Beauty Nail Products - Private Label Nail Products",
      "Description": "Scotia Beauty - Private Label Nail Products",
      "Keywords": ["scotia", "beauty", "private", "label", "nail", "products"],
      "Document_Language": ["en", "GB"],
      "Document_Type" : "Article",
      "Viewport" : {"initial-scale": "1.0"},
      "Theme_Color": "rgb(178, 0, 87)" 
    },


    "Social_Media": {

      "Active": true,
    
      "Graph": {

        "Social_Title": "Scotia Beauty - Private Label Nail Products",
        "Social_Description": "Scotia Beauty Homepage",
        "Social_URL": "scotiabeauty.com",
        "Social_Card": "summary_large_image",

        "Social_Images" : [        // <= More than one of these can be present. Any number (including all) can be FALSE. Only one can be TRUE.
    
          {
            "Active" : true,
            "Name" : "Scotia Beauty Social Image",
            "URL": "https://scotiabeauty.com/.assets/theme/social/scotiabeauty.jpg",
            "Description": "Scotia Beauty",
            "Type": "image/png",
            "Width": "1024",
            "Height": "512",
          }
        ]
      }
    },


    "Resource_Hints" : {

      "Active" : true,

      "Preload" : {

        "Active" : true,

        "Directives" : [

          {
            "Active" : true,
            "Preload": true,
            "Type": "font/woff2",
            "As": "font",
            "Asset": "/.assets/theme/elements/fonts/scotia-beauty.woff2"
          },
      
          {
            "Active" : true,
            "Preload": true,
            "Type": "font/woff2",
            "As": "font",
            "Asset": "/.assets/theme/elements/fonts/scotia-beauty-logo.woff2"
          }
        ]
      },

      "Module_Preload" : {

        "Active" : false,
      },

      "DNS_Prefetch" : {

        "Active" : false,
      },

      "Preconnect" : {

        "Active" : false,
      },

      "Prefetch" : {

        "Active" : false,
      },

      "Prerender" : {

        "Active" : false,
      }
    },


    "Icons" : [

      {
        "Active" : true,
        "Icon" : "SVG Favicon",

        "Element" : {

          "element" : "link",
          "rel" : "icon",
          "href" : "/.assets/theme/elements/icons/favicon.svg",
          "sizes" : ["any"], // <= Optional (?)
          "type" : "image/svg+xml"  // <= Optional
        } 
      },
 
      {
        "Active" : true,
        "Icon" : "ICO Alternate Favicon",

        "Element" : {

          "element" : "link",
          "rel" : "icon",
          "alternate" : true,             // <= Optional. But when present and TRUE, turns rel="icon" into rel="alternate icon" (Review this - is it actually spec?)
          "href" : "/favicon.ico",
          "sizes" : [32, 48], // <= Optional (?)
        } 
      },
      
      {
        "Active" : true,
        "Icon" : "Safari Mask Icon",  // <= MUST be SVG

        "Element" : {

          "element" : "link",
          "rel" : "mask-icon",
          "href" : "/.assets/theme/elements/icons/mask-icon.svg",
          "color" : "rgb(0, 0, 0)"
        } 
      },

      {
        "Active" : true,
        "Icon" : "iOS Devices Touch Icon",  // <= MUST be 180x180 PNG

        "Element" : {

          "element" : "link",
          "rel" : "apple-touch-icon",
          "href" : "/.assets/theme/elements/icons/apple-touch-icon.png"
        } 
      }
    ]
  },


  "Impressum": {

    "Created": "1544882400",
    "Updated": ["1544882400"],

    "Credits" : {

      "Active" : false,

      "Web": {
      
        "Active" : true,
        
        "Author": {

          "Name" : "Scotia Beauty",                        // <= <meta name="author" content="Scotia Beauty" />
          "URL" : "https://scotiabeauty.com/about-us/"     // <= <link rel="author" href="/author-page.html" />
        },

        "Publisher": {

          "Name" : "Scotia Beauty",                        // <meta name="publisher" content="Scotia Beauty" />
          "URL" : "https://scotiabeauty.com/about-us/"     // <= <link rel="publisher" href="/publisher-page.html" />
        }
      },

      "Facebook": {
      
        "Active" : false,

        "Author": {

          "Name" : "Alan Lansdowne",
          "URL" : "https://www.facebook.com/AlanLansdowne"       // <meta property="article:author" content="https://www.facebook.com/AlanLansdowne" />
        },

        "Publisher": {

          "Name" : "Rounin Media",
          "URL" : "https://www.facebook.com/page/RouninMedia"   // <meta property='article:publisher' content="https://www.facebook.com/page/RouninMedia" />
        }
      },

      "Twitter": {
      
        "Active" : false,

        "Author": {

          "Name" : "Alan Lansdowne",
          "URL" : "https://twitter.com/AlanLansdowne",
          "Handle" : "AlanLansdowne"                                    // <meta name="twitter:creator" content="@AlanLansdowne">
        },

        "Publisher": {

          "Name" : "Rounin Media",
          "URL" : "https://twitter.com/page/RouninMedia",
          "Handle" : "RouninMedia"                                     // <meta name="twitter:site" content="@RouninMedia">
        }
      }
    },


    "Social_Profiles" : [ // <= Intended as a more sophisticated replacement to <link rel="me" href="https://twitter.com/example">

      {       
        "Title" : "Professor Plum",
        "Relationship" : "Lead Author",
        "Social_Profile_URLs": [
          {
            "Active" : true,
            "URL" : "https://twitter.com/professor-plum" // <= <link rel="social-profile rel-lead-author" title="Professor Plum" href="https://twitter.com/professor-plum" />
          }
        ]
      },

      {      
        "Title" : "Mrs Peacock",
        "Relationship" : "Co-author",
        "Social_Profile_URLs": [
          {
            "Active" : true,
            "URL" : "https://twitter.com/mrs-peacock" // <= <link rel="social-profile rel-co-author" title="Mrs Peacock" href="https://twitter.com/mrs-peacock" />
          }
        ]
      },

      {     
        "Title" : "Colonel Mustard",
        "Relationship" : "Contributing Author",
        "Social_Profile_URLs": [
          {
            "Active" : true,
            "URL" : "https://facebook.com/colonel-mustard" // <= <link rel="social-profile rel-contributing-author" title="Colonel Mustard" href="https://facebook.com/colonel-mustard" />
          }
        ]
      },

      {    
        "Title" : "Miss Scarlett",
        "Relationship" : "Contributing Author",
        "Social_Profile_URLs": [
          {
            "Active" : true,
            "URL" : "https://linkedin.com/miss-scarlett" // <= <link rel="social-profile rel-contributing-author" title="Miss Scarlett" href="https://linkedin.com/miss-scarlett" />
          },

          {
            "Active" : false,
            "URL" : "https://instagram.com/miss-scarlett" // <= <link rel="social-profile rel-contributing-author" title="Miss Scarlett" href="https://instagram.com/miss-scarlett" />
          }
        ]
      }
    ]
  },


  "Document_Context": {

    "Canonical_URL": "https://scotiabeauty.com/",

    "Series": {

      "Active" : false,

      "Parent_Page": {

        "Active" : false,
        "URL" : ""
      },

      "First_Page": {

        "Active" : false,
        "URL" : ""
      },

      "Previous_Page": {

        "Active" : false,
        "URL" : ""
      },

      "Next_Page": {

        "Active" : false,
        "URL" : ""
      },

      "Last_Page": {

        "Active" : false,
        "URL" : ""
      }
    },

    "Translations": {

      "Active" : true,

      "en": {
        "Active" : true,
        "URL": "https://scotiabeauty.com/"
      },
        
      "de": {
        "Active" : true,
        "URL": "https://scotiabeauty.com/de/"
      },
        
      "x-default": {
        "Active" : true,
        "URL": "https://scotiabeauty.com/"
      }
    },

    "Robots" : {

      "Active" : false,

      "Directives" : ["index", "follow"]

      /*
      index
      follow
      noindex
      nofollow
      nosnippet
      noimageindex
      noarchive
      notranslate
      unavailable_after:[RFC 850 format]
      max-snippet:[maximum number of characters / -1 for unlimited]
      max-video-preview:[maximum number of seconds / -1 for unlimited]
      max-image-preview:[none|standard|large]
      */
    },


    "XML_Sitemap_Indexing" : {

      "Active" : true,

      "Content" : {

        "Active" : true,                         // <= Only the Sitemaps relevant to this page are listed

        "---" : {
          "Active" : true,                      // <= Very rare for XML_Sitemap_Indexing/Content/--- to NOT be true
          "Indexed" : true,
          "Asset" : "/.assets/content/webrig/sitemaps/xml/content/sitemap.xml",
          "URL" : "/sitemap.xml"
        },

        "en" : {
          "Active" : true,
          "Indexed" : true,
          "Asset" : "/.assets/content/webrig/sitemaps/xml/content/en/sitemap.xml",
          "URL" : "/sitemap-en.xml"
        },

        "de" : {
          "Active" : true,
          "Indexed" : false,                   // <= Even though the sitemap is a) relevant and b) active, this page is not indexed in it 
          "Asset" : "/.assets/content/webrig/sitemaps/xml/content/de/sitemap.xml", 
          "URL" : "/sitemap-de.xml"
        },

        "es" : {
          "Active" : false,                    // <= This shows that the sitemap is NOT being used currently, but if it were, this page is indexed in it
          "Indexed" : true,
          "Asset" : "/.assets/content/webrig/sitemaps/xml/content/es/sitemap.xml",
          "URL" : "/sitemap-es.xml"
        }
      },

      "Images" : {

        "Active" : false,

        "---" : {
          "Active" : false,
          "Indexed" : false,
          "Asset" : "/.assets/content/webrig/sitemaps/xml/images/sitemap_images.xml",
          "URL" : "/sitemap_images.xml"
        }
      },

      "Videos" : {

        "Active" : false,

        "---" : {
          "Active" : false,
          "Indexed" : false,
          "Asset" : "/.assets/content/webrig/sitemaps/xml/videos/sitemap_videos.xml",
          "URL" : "/sitemap_videos.xml"
        }
      },

      "News" : {

        "Active" : false,

        "---" : {
          "Active" : false,
          "Indexed" : false,
          "Asset" : "/.assets/content/webrig/sitemaps/xml/news/sitemap_news.xml",
          "URL" : "/sitemap_news.xml"
        }
      },

      "SitemapIndex" : {

        "Active" : false,

        "---" : {
          "Active" : false,
          "Indexed" : false,
          "Asset" : "/.assets/content/webrig/sitemaps/xml/sitemapindex/sitemap_index.xml",
          "URL" : "/sitemap_index.xml"
        }
      }
    },


    "Alternate": {
      
      "Active" : false,

      "Formats" : [

        {
          "Active" : false,

          "Format": "PDF",        // <= PDF is a Document Technology Label (could be XLS, DOC, PPT, PDF etc.)
          
          "Element" : {
            
            "element" : "link",
            "rel" : "alternate",
            "type" : "application/pdf", // <= OPTIONAL
            "title" : "My PDF Document", // <= OPTIONAL
            "href" : "/.assets/media/documents/my-pdf-document.pdf"
          }
        },

        {
          "Active" : false,

          "Format": "AppView",        // <= OR... the "Alternative Document" could be a View in a 1st or 3rd Party App
          
          "Element" : {
            
            "element" : "link",
            "rel" : "alternate",
            "protocol" : "ios-app://", // <= OPTIONAL
            "href" : "409128287/gnmguardian/technology/blog/2009/feb/03/web20-internet"
          }
        }
      ]
    }
  },

  
  "Document_Network" : {

    "Active" : false,


    "Social" : {
      
      "Active" : false,

      "Properties" : [

        {
          "Active" : false,
          
          "Platform" : "Twitter",

          "Assets" : [

            {
              "Active" : false,
              "Name" : "Twitter_HQ",
              "URL" : "https://twitter.com/my-twitter-asset/twitter-hq"
            },

            {
              "Active" : false,
              "Name" : "Twitter_List",
              "URL" : "https://twitter.com/my-twitter-asset/twitter-list"
            },

            {
              "Active" : false,
              "Name" : "Twitter_Collection",
              "URL" : "https://twitter.com/my-twitter-asset/twitter-collection"
            }
          ]
        },

        {
          "Active" : false,
          
          "Platform" : "Facebook",
          
          "Assets" : [

            {
              "Active" : false,
              "Name" : "Facebook_Page",
              "URL" : "https://www.facebook.com/my-facebook-page"
            },

            {
              "Active" : false,
              "Name" : "Facebook_Group",
              "URL" : "https://www.facebook.com/my-facebook-group"
            },

            {
              "Active" : false,
              "Name" : "Facebook_Shopfront",
              "URL" : "https://www.facebook.com/my-facebook-shopfront"
            }

          ]
        }
      ]
    },


    "Syndication": {
      
      "Active" : false,

      "Formats" : [

        {
          "Active" : false,

          "Format" : "RSS",         // <= RSS is a FEED TECHNOLOGY LABEL (could be Atom, RSS2, RSS2.0 etc.)

          "Element" : {

            "element" : "link",
            "rel" : "alternate",
            "type" : "application/rss+xml",
            "title" : "My RSS Feed",
            "href" : "/.assets/content/webrig/syndication/rss/my-rss-feed.rss"
          }
        },

        {
          "Active" : false,

          "Format" : "Atom",       // <= Atom is a FEED TECHNOLOGY LABEL (could be Atom, RSS2, RSS2.0 etc.)
          
          "Element" : {

            "element" : "link",
            "rel" : "alternate",
            "type" : "application/atom+xml",
            "title" : "My Atom Feed",
            "href" : "/.assets/content/webrig/syndication/atom/my-atom-feed.atom"
          }
        }
      ]
    },


    "Apps": {
      
      "Active" : false,

      "Native_Apps" : [

        {
          "Active" : false,
          
          "AppName" : "myNativeApp_iTunes__1.2",

          "App_Store" : "iTunes",

          "App_Store_Name" : "myNativeApp",

          "Download_URL" : "https://myappdomain.com/my-apple-itunes-app",

          "Elements" : [

            {
              "element" : "meta",
              "name" :"apple-itunes-app",
              "content" : "app-id=xxxxxxxxx, affiliate-data=myAffiliateData, app-argument=myArgs"
            }
          ]
        },

        {
          "Active" : false,

          "AppName" : "myNativeApp_GooglePlay__1.3",

          "App_Store" : "Google_Play",

          "App_Store_Name" : "myNativeApp",

          "Download_URL" : "https://myappdomain.com/my-google-play-app",

          "Elements" : []
        },

        {
          "Active" : false,

          "AppName" : "myNativeApp_Windows__2.1",

          "App_Store" : "Windows",

          "App_Store_Name" : "myNativeApp",

          "Download_URL" : "https://myappdomain.com/my-windows-app",

          "Elements" : [

            {
              "element" : "meta",
              "name" :"msApplication-ID",
              "content" : "myAppId"
            },

            {
              "element" : "meta",
              "name" :"msApplication-PackageFamilyName",
              "content" : "myMicrosoftAppBuildPackageName"
            },

            {
              "element" : "meta",
              "name" :"msApplication-Arguments",
              "content" : "myArgs"
            },

            {
              "element" : "meta",
              "name" :"msApplication-MinVersion",
              "content" : "myMinVersion"
            },

            {
              "element" : "meta",
              "name" :"msApplication-OptOut",
              "content" : "myOptOuts"
            }
          ]
        }
      ]
    }
  },


  "Document_Build": {

    "Minify" : false,     // <= If TRUE, this will MINIFY this document markup as part of the Flat File Stage

    "Scaffold" : [        // <= More than one of these can be present. Any number (EXCEPT all) can be FALSE. Only one can be TRUE.
    
      {
        "Active" : true,
        "Name" : "Scotia Beauty Scaffold",
        "Asset" : "/.assets/content/scaffold/scaffold.php"
      }
    ],


    "SiteManifest" : [        // <= More than one of these can be present. Any number (EXCEPT all) can be FALSE. Only one can be TRUE.
    
      {
        "Active" : true,
        "Name" : "Scotia Beauty Site Manifest",
        "Asset" : "/.assets/theme/manifests/site/site-manifest.json",

        "CrossOrigin" : {

          "Active" : true,
          "CORS_Directive" : "use-credentials"
        }
      }
    ],


    "PageManifestData" : [        // <= More than one of these can be present. Any number (including all) can be FALSE. Only one can be TRUE.
    
      {
        "Active" : true,
        "Name" : "Scotia Beauty Page Manifest Data",
        "Asset" : "/.assets/system/build/page/page-manifest-data.json"
      }
    ],


    "Stylesheets" : [
      
      /*
      There are three types of stylesheet:

        - Default and Persistent         :: rel="stylesheet"
        - Default and Substitutable      :: rel="stylesheet" + title="my-default-stylesheet"
        - Alternate and Substitutable    :: rel="alternate stylesheet" + title="my-alternate-stylesheet"
      */

      {
        "Active" : true,

        "Asset" : "/.assets/theme/styles/styles.css",
        "URL" : "/styles/styles.css",
                              
        "Title" : {

          "Active" : false,               // <= when FALSE, ignores TITLE; when TRUE, makes TITLE inclusion obligatory
          "Text" : "my-alternate-stylesheet",
          "Alternate" : false             // <= When TRUE, turns rel="stylesheet" into rel="alternate stylesheet"
        },

        "Media" : {

          "Active" : false,
          "Media_Queries" : [

            {
              "Active" : false,
              "Media_Query" : "screen and (max-width: 320px)"
            }
          ] 
        },

        "Disabled": false,              // <= when TRUE,  this will apply the disabled boolean attribute to the <link rel="stylesheet" />

        "Minify" : false,               // <= If TRUE, this will MINIFY this stylesheet as part of the Flat File Stage
      }
    ],


    "Scripts" : [

      {                                               // Giving any key a value of FALSE is the same as omitting it entirely
        "Active" : true,
        
        "Asset" : "/.assets/theme/scripts/scripts.js",
        "URL" : "/scripts/scripts.js",

        "Module" : false, // <= If TRUE, equivalent to type="module"
        "DataBlock" : false, // <= If not FALSE, overrules type="module". If TRUE, equivalent to type="data-block", OR if any string, type="[ANY-STRING]"

        "Defer" : false,
        "Async" : false,
        "CrossOrigin" : false, // <= values can be FALSE, 'anonymous' or 'use-credentials'
        "Integrity" : false,
        "nonce" : false,  // <= not really sure how this works
        "referrerpolicy" : false, // <= values can be FALSE, 'no-referrer', 'no-referrer-when-downgrade', 'origin', 'origin-when-cross-origin', 'same-origin', 'strict-origin', 'strict-origin-when-cross-origin', 'unsafe-url'

        "Minify" : false     // <= If TRUE, this will MINIFY this script as part of the Flat File Stage
      }
    ],


    "Progressive_Web_App" : {

      "Active" : true,

      "WebManifest" : [        // <= More than one of these can be present. Any number (including all) can be FALSE. Only one can be TRUE.
    
        {
          "Active" : true,
          "Name" : "Scotia Beauty WebManifest",
          "Asset" : "/.assets/system/configuration/progressive-web-app/webmanifest/manifest.webmanifest",
          "URL" : "/manifest.webmanifest"
        }
      ],

      "ServiceWorker" : [        // <= More than one of these can be present. Any number (including all) can be FALSE. Only one can be TRUE.
      
        {
          "Active" : true,
          "Name" : "Scotia Beauty Service Worker",
          "Asset" : "/.assets/system/configuration/progressive-web-app/serviceworker/serviceworker.js",
          "URL" : "/serviceworker.js"
        }
      ]
    },


    "Page_Modules": {

      "Active": true,

      "accessSettings": {"Default": false},

      "Global": { "Active": true, "Namespace": {"accessSettings": {"Override": true, "Default": false}, "Accessed_By": {"Ashiva_Control_Pad": true}}},
      
      "Modules": [

        {
          "Publisher": "Ashiva",
          "Module": "Ashiva_Control_Pad",
          "Active": true
        },
        
        {
          "Publisher": "AshivaStructuredData",
          "Module": "ashiva_Breadcrumbs",
          "Active": true
        },
        
        {
          "Publisher": "AshivaStructuredData",
          "Module": "ashiva_Organization",
          "Active": true
        },

        {
          "Publisher": "Scotia_Beauty",
          "Module": "SB_Body_Data",
          "Active": true,
          
          "Namespace": {
            "accessSettings": {
              "Default": false
            },
            
            "Accessed_By" : {
              "SB_Colour_Charts": true
            }
          }
        },
        
        {
          "Publisher": "Scotia_Beauty",
          "Module": "SB_Colour_Charts",
          "Active": true,
          
          "Namespace": {
            "accessSettings": {
              "Default": false
            }
          }
        },
        
        {
          "Publisher": "Scotia_Beauty",
          "Module": "SB_Notice::Brexit",
          "Active": true
        },
        
        {
          "Publisher": "Scotia_Beauty",
          "Module": "SB_Translations",
          "Active": true,
          
          "Styles": {
            "apply": false
          },
          
          "Scripts": {
            "apply": false
          },
          
          "Namespace": {
            "accessSettings": {
              "Default": false
            }
          }
        },
        
        {
          "Publisher": "Scotia_Beauty",
          "Module": "SB_Restricted_Access::Safety_Data_Sheets",
          "Active": true
        },
        
        {
          "Publisher": "Scotia_Beauty",
          "Module": "SB_nextPage",
          "Active": true
        },
        
        {
          "Publisher": "Scotia_Beauty",
          "Module": "SB_Consoles",
          "Active": true,
          
          "Styles": {
            "insert": {"after": "SB_nextPage"}
          },
          
          "Scripts": {
            "insert": {"after": "SB_nextPage"}
          }
        }
      ]
    }
  }
}

```
