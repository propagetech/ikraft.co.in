You are a naming assistant. Given a list of file paths and minimal context from a static website, suggest a new filename (basename only, same extension) for each file. Rules:
- Lowercase, kebab-case, no spaces. SEO-friendly and human-readable.
- For HTML: use page purpose (e.g. about-us.html, contact.html). Keep index.html as index.html.
- For CSS/JS: use purpose (e.g. main-styles.css, analytics.js).
- For images: use content (e.g. logo-infygate.webp, hero-banner.webp). Use alt/title when provided.
- Return a JSON object: keys = exact original path strings, values = new basename only (e.g. "main.css"). Preserve extension.
- Do not change path prefix (e.g. css/ stays css/ by returning "name.css" not "css/name.css").

Files and context:
[
  {
    "path": "404.html",
    "context": {
      "title": "",
      "first_heading": "404"
    }
  },
  {
    "path": "about-us.html",
    "context": {
      "title": "Ikraft: Top Interior Company In India",
      "first_heading": "AboutUs"
    }
  },
  {
    "path": "blog.html",
    "context": {
      "title": "Architects in Hyderabad for Project Management | Modular Factory",
      "first_heading": "Blog"
    }
  },
  {
    "path": "blog_how-ikraft-interior-design-company-shaping-india-s-aesthetics.html",
    "context": {
      "title": "How Ikraft Interior Design Company Shaping India's Aesthetics",
      "first_heading": "How Ikraft Interior Design Company Shaping India's Aesthetics"
    }
  },
  {
    "path": "blog_how-to-create-a-functional-and-inviting-space.html",
    "context": {
      "title": "How To Create A Functional And Inviting Space",
      "first_heading": "How To Create A Functional And Inviting Space"
    }
  },
  {
    "path": "blog_tips-for-creating-a-cohesive-and-stylish-home.html",
    "context": {
      "title": "Tips For Creating A Cohesive And Stylish Home",
      "first_heading": "Tips For Creating A Cohesive And Stylish Home"
    }
  },
  {
    "path": "blog_trends-in-office-interior-design-across-india.html",
    "context": {
      "title": "Trends in Office Interior Design Across India",
      "first_heading": "Trends in Office Interior Design Across India"
    }
  },
  {
    "path": "contact-us.html",
    "context": {
      "title": "Contact Us \u2013 Modular Furniture Manufacturers in Hyderabad",
      "first_heading": "GET INTOUCH"
    }
  },
  {
    "path": "css/4ba1f7eeea678c518b19a8a229705620.css",
    "context": {
      "path": "css/4ba1f7eeea678c518b19a8a229705620.css"
    }
  },
  {
    "path": "css/559e64bf161e61fa0aca6e864c78191d.css",
    "context": {
      "path": "css/559e64bf161e61fa0aca6e864c78191d.css"
    }
  },
  {
    "path": "css/7990ccc2b2d3db63e56b377738b004af.css",
    "context": {
      "path": "css/7990ccc2b2d3db63e56b377738b004af.css"
    }
  },
  {
    "path": "css/84d4a0216f16f715d9b301db3a8da352.css",
    "context": {
      "path": "css/84d4a0216f16f715d9b301db3a8da352.css"
    }
  },
  {
    "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css",
    "context": {
      "path": "css/99c4e6f40ee9111eea53b6472f3e60f9.css"
    }
  },
  {
    "path": "css/d09d646f062b67daeff66ff1410b63fc.css",
    "context": {
      "path": "css/d09d646f062b67daeff66ff1410b63fc.css"
    }
  },
  {
    "path": "css/internal-styles.css",
    "context": {
      "path": "css/internal-styles.css"
    }
  },
  {
    "path": "healthcare.html",
    "context": {
      "title": "Top Healthcare Architecture Firms In India",
      "first_heading": "HEALTHCARE"
    }
  },
  {
    "path": "hospitality.html",
    "context": {
      "title": "Hotel Interior Design Contractors- Ikraft Interiors",
      "first_heading": "HOSPITALITY"
    }
  },
  {
    "path": "imgs/013641c04e0f74f29e9641d8c7d31649.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0144562f50f70c036aba8b5abca009ad.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/033702b404875e24d90c353e314c9403.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/03f37ddd8e0222c004cc677e7e3abff7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/073a81f675eafa59a2e5e0a25d172125.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/073cd43a987ce3bdc9ef9c2f12569b7c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/07ccef174f5858f7e8e64a949d7e22f7.webp",
    "context": {
      "refs": [
        {
          "alt": "NETWORKING",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/080541f20a866304d17c8b9e6978593b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/081d07403d26966444bcb7c2cbc352dc.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/08d79f312c80272346dbadca3816b3b4.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/08dd829c801b70abca7ba9f7b82b272a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/090a8fa5bf45400d9c88eedd0cff9fbf.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/09c033fe1a0799ebe4fcce271ecb0f1c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/09c186735bcd18a5188e670daf27969d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0ac049c8610c652b7e6ed0842092cb95.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0b1b963d39bee73826b5592d09bc3f73.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0b9f000b29aba33b00371617b87b5e5e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0c34716fc2fed8ccecd7f4ebed8896d4.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0c6b7fbc41940af0e53886bec888e4b5.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0cf8ec7b66bd16094c7c63e97cdfa832.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0d7231d920056c69d43edb15d9730150.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0e0ffb3a86c77166f77da71299b59ad7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0e83da1e10f06d0bfcb98f2f5eabad03.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0ed9b605998c53f4594258de46d50de3.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0f05d5ec5dd8b312b6bd2e9bce1f99e1.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0f4013eb3c8b6b3b955f920aa021be00.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/0f7af731b61f6567317ca9949561e912.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1041e3e2d35d0c793c2b4594097d1136.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/10c86b308d4dcb7816349f725b75ea52.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/111f5d4c3ada7a8593c6f8c48d11eb15.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/11205ba9da4e59812057f35c7f70ae8c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/117f7738d0d03415c859029b6c003a27.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/11969d201c70f7e136670f97f4f8d66f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/11b7b5eca41a643c0a2b78a23a52ce29.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/12378d35ca69c55158a1e38f2da0acb6.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/123e827e97cfbc1d9bbec3f5973ee88d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1335da35900279a32e1ccd0eef081e14.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/13c39b4a3c1edcb954bcee2009903029.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/148a8afcd28b8c3343819044e358db87.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1528cebe619c16e1291ce0858d14ad29.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/176d80a43eaa32d143e9471e426810ca.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/183b29a80eb88df184fd8f4420204f3e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/18c107a303de1a2e48683e74d032cda8.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/193370be653b8e912e8fde634ccfbd89.webp",
    "context": {
      "refs": [
        {
          "alt": "image description",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/19c02ae48a74a0b0a15c59b9a3ea880d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1a2838a69e9fa2edebef23e7e7a4f1bb.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1a89f53b2872766d4a481fca52b153f3.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1b2b1ee4d66c57bcc9ce39c954a7e1a1.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1b2bb62616fec3ad38e591aa86a99ee3.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1b96680e7ae1590b3a784f028a033059.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1bf48c06f36d72ad3e9992e0b1f0dcb0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1db15ffcaa6bfe7cfe115105f7d14208.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1f2cd6ae3bcd7ad4b739922ac516098b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1f91f64f520564b047d8961509a0577e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/1ffbe288036c9adf4555b2c303eede48.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/202f0183d744b158e02d4a933968b0c9.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/20b2c6bc7280e30f861cad4d1c388d73.webp",
    "context": {
      "refs": [
        {
          "alt": "CivilWorks",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/213f9c82395de4833acd82481fccf8a2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/22871edbe7335a8f4ca41b1a4225db6f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/22cb78c7d2a2f38e3e35bf5b77cb02b3.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/233eafaf1927226c57f2344ca6e96727.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/23fa12f7604d577859056dfb9c7c8454.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/241a0098d0e39750420d3cc6197efea7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2460ab2e899f85ee09f16ab4f44e0ea2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/246ae788dc14c79c1246bca9e2858dcc.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/250e5f5a032e4574c7a02c1e7435c266.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/251d036ec5e9b0e16e0ac32c14ea4373.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/252ef5413712230dda9ddad7d126ec4c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2530cec80dc541cd88fa71eb498c687a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/269defe5c26e56083395278bbf99b45d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/27767fc2558a41db35d0d4085e255419.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2781d9a53a9ff6e832919a41ff27e27f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/27eabcfdd63d9b4d3f8e94d6bf8a8b14.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/280cc49ce2bde04b4ee200bf97493c06.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/28d1a6283e07cb9fa34d9f39a8b7b18f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/28f711733570334399dfdd0c1fb30466.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2980d621d8b85676546eb94734e058cc.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2b7cf02ebf852475219a08da58e8c9bd.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2bcd1be0039d61693df5950a12f25df5.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2bd98ab5ef97894d4239ea1f2ea64a4e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2be58b98a6fe4ec47b87037e1e92829c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2dd29b1dcadd9edfaccc17f2c0ae2cd7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2decee7f4247350ef9b4f956248997c4.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2eb0b949ff4f7338324aee160b9e61fa.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2f8607ab967a370274d16f5d9e7562d7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2fd2e444ee8fedd9d0701f0e1c357443.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/2fed177c9587496d0bbdb641dae24e8f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3069d55ee24c3317c0f1299cfc7c841e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3090bb3ff6cd3ed07f8542dc396c8169.webp",
    "context": {
      "refs": [
        {
          "alt": "Trust, Quality & Integrity are built into every project.",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/30ea178950a8596abd98e481c0ba7ac1.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/312522d4a41c1ccc30d0f16c223d4ba1.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3136d43ff3ae94611a8a97d43790e111.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/32cf2850b63dbf45f5078ba1b1e099b1.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/32f7838b194227002421dc0cd82a42d4.webp",
    "context": {
      "refs": [
        {
          "alt": "About us",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/34916ea48d9f95e35614550eae11239d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/34f4960285aa77023388c9d21d13a420.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/354e01fa7b84ca82e939b5260bf73c98.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/357661cac932fe49f55e73d246ae6911.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/35c507c5457007f395c849d450036a55.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/35d5d42bd833d890179573ece0b161ed.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/36c29c0dbae4e2e3ccf959036d0213ab.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3717da08f762e433377b90b3f37fada6.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/37218613bd8ed674e2c07aab1d449298.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/37b9fd5a116ef633e585925112bee5db.webp",
    "context": {
      "refs": [
        {
          "alt": "RETAIL & RESTAURANTS",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3833740697d770966a4b1ff2435fdddd.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3844bc39d37547b2426a366c1e02f249.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/386e3be4ebb4e0062d98ced4a8790e1e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/38e34335dbed1e6db24b5d2449a261e7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/398e00fb896c4000e2c2a8d44e2654e2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3a4dc934b5186bba58cefed32a185269.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3a4e82c73298fd8bacd4beb85c351fd8.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3ae638cbf3fada374bd91690d550b155.webp",
    "context": {
      "refs": [
        {
          "alt": "OFFICE SPACES",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3b5e28261fc287435c049d3434faa4f2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3c2fa2b6ea9f032505cdb93a2dadf1d0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3c5536dca64b6857915f21a973470b20.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3c64a81c1038f364b64bde3b769caaf7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3ce126eb420cc05cd283046931591206.webp",
    "context": {
      "refs": [
        {
          "alt": "FalseCeiling",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3cf6637373abc2df34cb1a4bb115a7cf.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3d48cedc33ca59fa4bd2090770cf2a9f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3d80ce97228fefe343821da143d137e5.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/3ddaa5d2a3c11ba717e4630ceaa80cf4.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/410b60501f56afd764dcc965fb485770.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/41a671f3137a01df4b194f77d2ffc990.webp",
    "context": {
      "refs": [
        {
          "alt": "Ikraft Interior Design Company",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/41c0308042c8b9220ec2fef1c7c11271.webp",
    "context": {
      "refs": [
        {
          "alt": "blog-thumb-1",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/41e06daa18e5f6754eba8ecf1cce90f1.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/42b742bca37fbfaf8d004c5a5abcd8eb.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/42dd97668ba82f7bc97ccb6203b0a2b2.webp",
    "context": {
      "refs": [
        {
          "alt": "HEALTHCARE",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/433a69a93e1de48e9bf86877ad00e187.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/43b2f89276b81ef6ddc18d92c99e122f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/43f2ca9db6461235298966ab3fc132d7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/44e86531b818d72903bb9ad1c7d81e46.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/466ffd39a0019185d34a6bc226d6a64a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/46e2a71fa24a9c264b18e8413a5212a3.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/473fca5336f91b03b4c42a72c4e307e0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/47731231d197139ef5ddd27bffc2af3c.webp",
    "context": {
      "refs": [
        {
          "alt": "FALSE CEILING",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4791e21b1b34f3b6668d78641bdfd1c5.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/47cbf25f4d13174f14c25f5f386460ea.webp",
    "context": {
      "refs": [
        {
          "alt": "CivilWorks",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/486fd847e15adada619d310251e55e8b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4911e645cb6309cd1234d457e0b927ee.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4a41969891c46e22b868cb66d536137e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4ac7c32e64b3dea08da1bfa61e49465a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4af24df10a459a31aa264add3f81eb17.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4bee6d1d96870e6236693b17bf5b080f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4c9d28e9a3d9244d11d880ca68b34995.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4e26210449a1394a3dac3acb4b8d7819.webp",
    "context": {
      "refs": [
        {
          "alt": "CivilWorks",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4ece8855af648babfada13b44d1d1777.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/4fc15e422de539680ad88e018a3247d3.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/502909446312c98c88bc732979c5d230.webp",
    "context": {
      "refs": [
        {
          "alt": "OFFICE FURNITURE",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/50674965b0b16bfeae88031a2437837b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5073b37d1d874fcbf8e735794e652e7e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/513bacb16e8504a91931a4c988473321.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/520149cd181f41980ca1a156e675313c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/526e1da14b1a4ac2822f800ae8e79664.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/528a8b5e2774085e285d05fa97eb1978.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/53634635a2c822e31cd66b6d05618a21.webp",
    "context": {
      "refs": [
        {
          "alt": "FLOORING SOLUTIONS",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5373871d33432c82701ba7fe351c08a7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/53aa3fc384ce2b882a5ecae452b7757a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/549825b8ba5b0ecf2ef1f66840a13e25.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/54e9fe1acdfde420029773a48b77771e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/551c39c9a15205ae190f5d79e00eb86e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/55377f2fc83236e9f14ebfd16492ec28.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5649b9f5171792ba7affe6826d45dace.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5678a550f06fbe3d07295b57c68b761b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5692717202b5544b040594d7971964de.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/57068d1807aca4e9ab8820b4ccd911bc.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/58188f4a9ef3a749e61f6a8283c176b2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/583988ec4591a129e9f78d661d10f098.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5a249c084e0f0e5d9ae4caed6f96645c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5abff6beae13c29b91eb9ff2ac88987b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5b1e65fa801a149a06c3ab3077a56f53.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5b25b2e77299597ee1b66939177ede43.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5b95af3987ae2143abd3c93720676b44.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5b9a30f31cbaf223c6c7e23d604368e5.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5bc2dfde5409d2faa4a740ca45b40224.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5bca539002f8e83d3857128a17c292a0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5d6d7ab20b4d19a44db252ba0cff8703.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5d95eb6bf5f470ee770bc40aca49a022.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5db9474f1cdb9cba55d4629c6d585729.webp",
    "context": {
      "refs": [
        {
          "alt": "pantry4",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5e1546134d36bb8d30a626498b1d80e1.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5e95182de781f06db90e6565425466ca.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5e999cd7724add126ad5fb87e7c41244.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/5ec3d1969dd81bfa96b982e720421ce1.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/60e283c8f41432dd24fdcd1f24df81f3.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/60ee6338d8231e1db4b8a13c05b760ca.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/616c130a81eaedf8264a21e82f6bd323.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/618f8d47604a0703958d6533975ecfb8.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/61ad1704b4d03da61745a0839b11344d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/621d695c90571bd3d65997ac393d994b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/62fef4a726f988f1f431d1701d4aa896.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/63bf1c624afb9d8fc3271ac393775f71.webp",
    "context": {
      "refs": [
        {
          "alt": "About Us",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/63e43d0c24e613f2161abd606e4482b5.webp",
    "context": {
      "refs": [
        {
          "alt": "PartitionPanelling",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/659cd93cbee94450acc61a508c3b1cf8.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/65fad0fe4813f57e3582492176cf08a3.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/65fb7aeb617ada9414210b58de3fc898.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/660523fb2527e512327bd5fb3eb1265f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/662c0f57b384140e1cace6b5160fd8c4.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/66aea744235ef7b584aceca5beb606ff.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/66b96a2f8bc59c16ec20dc66e5adb0cb.webp",
    "context": {
      "refs": [
        {
          "alt": "ModularFurniture",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/679cf0dceb9a08ef782903c0ed392cb5.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/67e1eb516c22929323e40b144bd0b970.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/67eed46a4157cd643884cad18d6acf4b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6848dee772be15ced3fe724ba275cf21.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6a28df7862572ed57d860c782e89af52.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6ad35692739b48497b52e6cb23a5dd85.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6bdbb00ae556764f14229732c763ae52.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6bde5262c071057b57df8e6b5a8a7128.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6d3c88f42ff1676a4a0300539d347074.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6ea1ab65ddeb450942bb8e92ca28f516.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/6efe49ba8c48514c5d1437536faaaba1.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/708eb29013c5457c616bdd49416e8633.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/709eabab06d0407acd90904d0c0e8401.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/70f1972a3f9bcc0ac238bb2bb817ea7d.webp",
    "context": {
      "refs": [
        {
          "alt": "FalseCeiling",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/70f820e3778067f3ceb307f73dcdb587.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/71578be50385abd7ee2212418d139945.webp",
    "context": {
      "refs": [
        {
          "alt": "image description",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/724572de2fb0aa220030d56c613053d6.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7273839aa5004d11bcaba195d2969f2c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/727a9285ac26bdf82f1867de7399671e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/72e712c817bb9b7d5ba8691c29e833ee.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/73114231ffffec6bfde4805416336bd9.webp",
    "context": {
      "refs": [
        {
          "alt": "RESIDENTIAL",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/73298e077c5b21a68e648c1ec14ea782.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/73b0c89afbe0557d0dbae97052825bb2.webp",
    "context": {
      "refs": [
        {
          "alt": "CCTV",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7467f2cb7086bbb869ad9f84c4c175e3.webp",
    "context": {
      "refs": [
        {
          "alt": "work10",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/76410a20c35c9c34a6dcbcfa8573cd54.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/765a4ef08a2e95c7b93ab1c3e81578ca.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/77377fdd9b90bfec8631eeeaf4a709b0.webp",
    "context": {
      "refs": [
        {
          "alt": "HOSPITALITY",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/780ad670e89829be5d71bffd30f77d8c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/784dee8e6ba03c01108fe1918a5fcc17.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/78676932451f3c092090d38b857aece1.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/78c41ca3acae156de18be25ec0e982c2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/78ef776dde92294279abc9ed9a89f301.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/790d511a66ef69cfc80d41341f7708cf.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/791784bc164db34cc548d90cd6da488b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/793b8055f228fa2d93228ae7a59a8149.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/796d345a93d18f54e4bb0e5b618663df.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7a1ee097b74fc78cf3f76a07e0d85cc1.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7aac5891771e53b1e1d023fc62cad2fb.webp",
    "context": {
      "refs": [
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        },
        {
          "alt": "logo",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7af46d23724ed6690636347c7355bd14.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7bc1481e86a0a47b25fea9d3f25435a7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7bca16bf3dc3de7ebab9a3220fcdf7f0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7bd567d2668916476bba18097158ba52.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7c4e358b38290f0d585f92d841ec4abf.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7d0497cb7faff635aaee6b23d9efa334.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7d33cdf11053ba52274d7c4cf83ed5e2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7dc40c5675f3d30b0a58d8ec71e18de0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/7f7671baca3dfbacc725c856e63bff45.webp",
    "context": {
      "refs": []
    }
  },
  {
    "path": "imgs/7fb92a690901901bf8a196bd471212c7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/806ff0453b0a8007e41146ebf1ac4d94.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/81501f281bcb629c3b8956adcb04e00d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/81a919e3f15c1f60b6a1bd5875eca746.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/826834b54204525c672dd7ae111271bd.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/83af9750049da06efd445230f789b9a8.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/83d8027a9ecc5b773590566ab6bd0e29.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/844fad9b75e1c584b5f4cf568c6b079f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/84770ae078f74d383f955cd0ca0ad421.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/853e0e881078189261bcce6ce1181b00.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/85b5dcf7dd00b053dd63a43319cbd84c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/86048ee2168f81707bc4fbe9c78ab7f4.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/874da0486d506a2e1dfd52c456362822.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/87ff752733b671963ca1d54249f9a5a0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/889e137a6535d1290058e999024ac510.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/88a0cfc678319f525fc3bf14af0176cb.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8a67dd05efe61b9916ae8c3d20a0b440.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8b851e4d59ab21c9c1b8d837dac39356.webp",
    "context": {
      "refs": [
        {
          "alt": "image description",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8c31531198dba9928a3908967e1e0d59.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8c52a93405cc20d864eb0dce8e117e23.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8c6647f988c825253a1ebb54bc773922.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8cbe9f50652ab4d8127f8c206aa32902.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8ce0a4a70d0b0c98ad63fad70c754ab9.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8d108f78945d90400749f359fe9ddd23.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8d62915af3adefab7ebf689d38d5c2a4.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8d84ed13a9cfd974a1e92f2a7ded5f2a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8e64899823600f8f3ba2a463897aa625.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8e79105af831ab5fe28bdc4160999c9f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/8fa0cd63d7e3308e60d3a3dceeb019e1.webp",
    "context": {
      "refs": [
        {
          "alt": "FABRICATION WORKS",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/900b4f7c4ffac0d8c6ab8ed95f958074.webp",
    "context": {
      "refs": [
        {
          "alt": "PARTITION SYSTEMS",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/904bf00c954a8a5961d1b6149ff0c333.webp",
    "context": {
      "refs": [
        {
          "alt": "PartitionPanelling",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/90caa4d273ef271c5449c61c91fc3747.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/90e88293c431fec38fe497f87f60b780.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/90f654fd8ba1c3f969dbc501021d4068.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9121217b491d8ba370f599cea5aa5c96.webp",
    "context": {
      "refs": [
        {
          "alt": "FalseCeiling",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/91cd8f31b56bc2884185fd4203d2f313.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/92a485106bfc2b9139f780b7d2950b59.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/930344246c7a3a053f3841eb1221fe01.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/94498064be8c5ea705f0f6eee6f96bac.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/952f7d7b14c5b9266fe6386a8fa0cff9.webp",
    "context": {
      "refs": [
        {
          "alt": "CarpentryJoinery",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9641fc8e70bd5d12fb5a1da6d02c4b66.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/966928578f9247eed930e87b0a0e83e6.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/976a5a03cfcc51556ecc25e3a20c1132.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/986294042205f7d3897c2f739c3f6632.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/990d6e38a265202bba3ffe0c58ca7498.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/992612c15d9dc0f1f134d6c71cc7e1a9.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/99473613d53d42b51a156f624c89ec7c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/99e4aa3f4ae19de5eb73147a5b7c4bc5.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9ac8adcb7a844e95b9b87da8c68a607c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9b14c297359fd043ded963521ffdab7a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9b2b09f974c005ebef698950b2fe3343.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9c2c700727aace9c97b2efbb73a0d7ff.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9ca0d5e3837bb5faff92853eca78497f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9d203f52cb6b47cace1a01f9cd8677da.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9dd33b522b71681ce0a2b80ec326dbcb.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9ec9c6674f1e48090bdc8a00fccad2a3.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/9f1f045b57a231f56c7b755579879597.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a0ba1bb579ae3f038a13aa8db54d599d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a0bced6780979767ca44f8a202414ed3.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a0dd4a0f67bbb8fe441a5105cedbf892.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a105bc9b28e1a809117f85614c7aa1ed.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a158da566098ffccb4f5dd1a80501083.webp",
    "context": {
      "refs": [
        {
          "alt": "PartitionPanelling",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a15946bdc9a13942d5a28c115b6c2a15.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a21ef04c1289c5e6434957e0c7ec387d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a278ec93df1ea116564fa27cb1be16f0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a327f66a91d30ef2730060033bb6b077.webp",
    "context": {
      "refs": [
        {
          "alt": "HOME AUTOMATION",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a41b643e72aa0b3483dc92393d477c3b.webp",
    "context": {
      "refs": [
        {
          "alt": "WhatsAppImage20221101at44132PM",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a47d60856c258d055997c55a9e308501.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a4cbf7f7efbdf40f319a8d7b623125cb.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a57104a12071407fa2ecb1cb2a8959b9.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a639f44e55bdb70c50213e81cc6b3ce7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a67b6e58f06c14bf77695abaadf6c16b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a6ce1768f8768d90ba6b29edc0fe8045.webp",
    "context": {
      "refs": [
        {
          "alt": "INTERIOR STYLING",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a6e132e50702f34df58280f5d2f50fd5.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a81f9e48fae141918e001110e5345c96.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a831863766fc770be3471b11de9b7372.webp",
    "context": {
      "refs": [
        {
          "alt": "CivilWorks",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a9d2c3674357badef06b1efe816b168b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/a9d55959306098bd4894c079749cead3.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/aad67681999a922e686cd760cf10b500.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ab23aae197f3898da0a4d9144811d24e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ac1e5bef7f83b0e8de99a86bdbe8ccdf.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ac4542ddf0f929d6487a03028cb42ba6.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ad5856464a889fdb9bcfdf9a75154649.webp",
    "context": {
      "refs": [
        {
          "alt": "CarpentryJoinery",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/adab0ad2899288a3f2dfe6f4fdb48cb5.webp",
    "context": {
      "refs": [
        {
          "alt": "PLUMBING & SANITARY WORKS",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/addbbc66360f87e0731847147ec802d7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ae0a1a8852897a0c7a2748e7823bbbe2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ae48e2217b3a29358b79bf69f159f5db.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ae5ec56544fbb4705ae976aa0626f015.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ae75a41dc79dbc0a5bcfc154f4de45b6.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ae7608bf5e09e9925576d5c8e810978a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/aea6aa48961a050b1f4f8e2c2f6dbfd2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/aeebb9960103905461e6d1811c1f1f26.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/aef64db248e156481f6c28f2f1ffd6c7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/af7f4e8c87b91b6b756923cb33bec082.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b05c950db6e30408436156b3a3c361a9.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b0641c929ffe0e387afa211f23bf009d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b06ea558bb92db5f68494ed5ad39e9c7.webp",
    "context": {
      "refs": [
        {
          "alt": "HVAC",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b0d8a52af9705875479716cc31092feb.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b0faba0ae18ab1587aa1af5c5cfb95f0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b0fb307d5fe03cf87922045d821f13f1.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b15974a7249e9fdd3be1aee4e8e47e47.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b1f94564a09351744d6ce71877f22819.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b257af73fa622d3abd64c60914fc53c0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b2d728eedb4311a39134aae0ddca97b4.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b3a56806d4e0cc4e5641085b610e0e99.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b4bc7bfdeeb1ace27d3599f4232ea25c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b4d634b39ca40634f5e2a355faa5c258.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b5a0dcb490b062343ac2d6cf0a470a25.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b5cea6b07e7cb8805ab5067892064639.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b683b14e79c374974c050b1362368b49.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b6cd9e65a3cb643d1de2467d0bf383cb.webp",
    "context": {
      "refs": [
        {
          "alt": "CarpentryJoinery",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b70fbb5b75f8d8d56fbc9b6729ebe7ed.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b78b4390637889f952f152478da35473.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b89f1173ecf4395a0ba6d9ba72403d03.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b8aee9a5c99910f090728ebec7f49d62.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b95a1d5ba684f0ce7b847c26c81d4dd0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/b9fea58d36e93f17c7a6ac3b65785108.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ba7b70d2afaaa8f9d28c88d6e792fb78.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/bb48640126e1934535e1b767bb8702aa.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/bbb94fb7d433bd2154568f4ca38f8ac6.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/bdc2ad5244a8f27afe3bcf3080d44cb4.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/beed3a30e2163f906bb9a5af74630950.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/bf1a60b9f2ec3829fd08c98f5dab4b6b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/bffab9d33b4835e01a026915c5c27b59.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c0268df577d7820d52db73dc397a16ee.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c111706581401513f889ad86f210c53a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c13d9ad16d89413cf291d20fe8ab067f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c13e07982f1c352d99d6248f4ad89741.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c1d66ef4169784d19ec67d935f000e99.webp",
    "context": {
      "refs": [
        {
          "alt": "PartitionPanelling",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c4002d18c4c7f0940ea2229ec0e6c0b1.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c401e275b1dd05ae6edf0ea5c5145f23.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c48cccd024b58a4ab726aa4c533b9bd9.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c4a0f610687c623262e975a90e3f463e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c4ed68bd23bff0b184ebae5105f278ec.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c55191551387e3c229809c1dfb496f81.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c63bd3f0a4a6d437efe08b26af8cf120.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c76c81e717f795ae4ae2f1ca4e27daed.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c7b1497524dfadaaff03f250e3ea5a89.webp",
    "context": {
      "refs": [
        {
          "alt": "ModularFurniture",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c7bf55deeabf8fb1567bfbee1df63206.webp",
    "context": {
      "refs": [
        {
          "alt": "FalseCeiling",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c841572fde8d5afbcabdf889715e7e5a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c841c6451857971d0240fb0f84efcd13.webp",
    "context": {
      "refs": [
        {
          "alt": "ModularFurniture",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c848effeec41b5017c8c38c90c027e92.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c8f0166a1a969435a3ec6cf43ff0d481.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/c9d3e33f0ae0b2dad32d47422da7de36.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ca353e94631f93323910a0610839dcd0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ca87d1ff25a71f5eab82dbecca19b3e0.webp",
    "context": {
      "refs": [
        {
          "alt": "CIVIL WORKS",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cabddcb7fe4c19248366ba5d6bbb4225.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cb2619294957cd9455161c716742c93c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ccddc10841fdea2c2aadd909a88a8821.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ccef49423e3ed3724c916555a153e9a2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cd37b9964ae9901efa8007fe5b5cac75.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cd647cbd25c640655e9771034677050c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ce6eb068f2538a589da21e6446d750b0.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ce9b1990c408813c89bb714a54955574.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cf05d10baf31ca54c25485fc41f43b91.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cf56699c6fc1d5469214ba9feabb2bf7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/cfa1afc1baf3ab7457eafbe853339281.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d051d503666f5d97d53c5e161ad54d38.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d0e6dd5c2884f2c83039369d18e8acd3.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d1296558d600f7667b5ff3de96d819cc.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d144a0dfb54e95694d965991b5e24563.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d243a09d49a16f5d29b58ad66badbde9.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d262d6069f4a3cd825ba798b1ffc221d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d27f289bcc12f9d8f1e4730b514c394c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d2b7889b811fab54d10b5f0c6b11f28e.webp",
    "context": {
      "refs": [
        {
          "alt": "INSTITUTIONAL & COMMERCIAL",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d3f7d11a8b644f5243010784ff663759.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d433f0f59962b55236e5d65946625f3e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d4b9f1aad1e5918cfdd0193aa89cf8a9.webp",
    "context": {
      "refs": [
        {
          "alt": "JOINERY & CARPENTRY",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d58eaec4f8c0fa10f43a448140d327b5.webp",
    "context": {
      "refs": [
        {
          "alt": "Diversified Services Unwavering Quality",
          "title": ""
        },
        {
          "alt": "Diversified Services Unwavering Quality",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d609f10ec7f2f0374b2d3338ae188dd3.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d65eecae0b9bbb835403cb6677247a5e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d70e869b8291126e232c04c7a657f1b8.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d72dbfd928281b58f2166ad5c0e72ed2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/d97c9b1895023ea3b98b27fa90f3772f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/da0541c221e645abce276640bf5bc452.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/da1cf804fb1d5b5e952d7b763e25f1b2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/da69be73eaab1a5e09b443d2d7decc8c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/da6a0edeb9b31162bc420354df963cbe.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/da9067f53ec2f777fc879a531a5e4f95.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/dada43438b7ed1fa644eec092156abae.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/db606c9f7fba5d9d66fcf20f06bf70f6.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/dbfdb0d231ed01b34c1225d3d1bd83cc.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/de4461fe41db39ef45f640186fc0a0bb.webp",
    "context": {
      "refs": [
        {
          "alt": "blog-thumb-1",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/de7b7c4cbaf7d1260526de7f461311da.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/df3116c82f234ccfd5f0aa2e2cc4bffa.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/df620c4de823f8093d78910758aa59e7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/dff2b393e26962f09ebce20b9259ba83.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e08ee73391d0268096870be2cc03514d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e1b0a8f0d913bf431c14d2236da82619.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e1b44e9ad404b4f2d4333460624d18ec.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e1c341ca91817b1a14405ef65eef4754.webp",
    "context": {
      "refs": [
        {
          "alt": "image description",
          "title": ""
        },
        {
          "alt": "image description",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e21a37d53f11f7f4d1c1bde5d630b255.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e45b85cace770e150cdedb176efa4454.webp",
    "context": {
      "refs": [
        {
          "alt": "pantry8",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e57e41842451c529ba54862c08af7ab7.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e5a7c0ef4b8f121f89088034197de89f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e5f4330e1a3672153c52222e385a2cdb.webp",
    "context": {
      "refs": [
        {
          "alt": "INTERIOR SOURCING",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e629805bee650aa861accaef502be7f9.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e6d5828b8491b6b50d2f46f7cead1696.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e7e6692050b2824a3685623c7d5b9aee.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e96e871dc1b57de89a5e862c68ea011e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/e9e44153b59307ebe5045c345c6fcf09.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/eabf83f8899b430d8a046fb756a061bf.webp",
    "context": {
      "refs": [
        {
          "alt": "ACCESS CONTROL",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/eb018d1e1422c2105a697f505ae5789f.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/eb3065d56d99cc68ae5d72e3d19d5a7b.webp",
    "context": {
      "refs": [
        {
          "alt": "LIGHTING SOLUTIONS",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ec9b23ca24e4a0c3f0a8a59e4c5440e2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ecd6d7cccb94b89d4add7eae19357dc8.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ece8584ca523f1a534c8040d52d227f5.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/edd716bbe3c003ed2ece70655c3ea52b.webp",
    "context": {
      "refs": [
        {
          "alt": "PAINTING WORKS",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ee5c964dd1c037bc3efcff87002e20b1.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ee9d0de7e9c62d7a124c388a924fcb01.webp",
    "context": {
      "refs": [
        {
          "alt": "PA SYSTEM",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/eed6df1bce854f921389eacf4a9fc639.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/eef7b99ab2b051444776cfc8b6c972fe.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ef088d8763dfdd79a759d01c6f5cca1a.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ef66996f1cb8b67e4e7f0d6f9d315af2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/ef6d2300729b72a54ed8a7e30162cdb3.webp",
    "context": {
      "refs": [
        {
          "alt": "MODULAR FURNITURE",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f01100291bca29881508b4367240b0c4.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f0e31e113cfbcbd0099b406dee301f67.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f103051b265b6f112ec4525695f068c2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f1407c6698ecb56f7c5f7dbe6cef57af.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f14508752bfb070113f7a6a463a6fe59.webp",
    "context": {
      "refs": [
        {
          "alt": "CarpentryJoinery",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f14d449b64ba81186ab9636df3bba791.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f15d4c2dc08e187f99f058b37d3a9c46.webp",
    "context": {
      "refs": [
        {
          "alt": "ModularFurniture",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f1683cc69c1006a3bf090c03208cde7d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f2542b6a8acdd3a2c4633efc88ffb157.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f28abfc8649891c5e6e082de5c1e49f9.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f2a7b2939c1ffbc42a43861eec6ebdca.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f30b110e947459247309b487c665056b.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f3b326bdfb5b01c6e59e359c718ab156.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f47211b7c6d2ef3405442462e3035a18.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f4976dd790586b1ff89fb5036d8154fd.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f547dbcfb25fd4c023ce5bec444c17ce.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f582f40e567ac51b58e573e0980957ee.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f618e816c82d842d5221735a22f29ff5.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f6d242b8871e135c0e30f404961f7729.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f7816ba79816c5dd2d9a5199858e3de1.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f849dc09cef6121ef9243db2b93e7f5e.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f9d14a3860e9f3aa921452ca848e82d2.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/f9ede7e937e68a8f08ac5116276a9308.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fa881213b7f20f41b289d635d53ab32c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fb923986fbd3ea91aec4ac1d59d5d76f.webp",
    "context": {
      "refs": [
        {
          "alt": "ELECTRICAL WORKS",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fc05ee83562604635dd33d2328d48294.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fc872e1b96f4d610cf7992b6a11df0ac.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fca61b5a83285acceb8b406d685bc2f9.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        },
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fd9ea6e6aba13aa556671a353913edb8.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fd9fffa16d0631cc78ffdce8bba71b1d.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fde4885140a13829472d0cfe5dc352d8.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fe31a2565aca986013f3b37d701648bb.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "imgs/fffa6f9ad38349234d00548e0fa7639c.webp",
    "context": {
      "refs": [
        {
          "alt": "",
          "title": ""
        }
      ]
    }
  },
  {
    "path": "index.html",
    "context": {
      "title": "Ikraft Interiors \u2013 Interior Design Companies In Hyderabad",
      "first_heading": "IKRAFT"
    }
  },
  {
    "path": "institutional-commercial.html",
    "context": {
      "title": "Ikraft- Commercial Interior Design Services",
      "first_heading": "INSTITUTIONAL & COMMERCIAL"
    }
  },
  {
    "path": "js/03b2eaae6007054a68c38e495f894dba.js",
    "context": {
      "path": "js/03b2eaae6007054a68c38e495f894dba.js"
    }
  },
  {
    "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js",
    "context": {
      "path": "js/0a105d712b6a6c836c48dd97d0f0cac1.js"
    }
  },
  {
    "path": "js/0c46896987137b0016246f6bc2243099.js",
    "context": {
      "path": "js/0c46896987137b0016246f6bc2243099.js"
    }
  },
  {
    "path": "js/165d7b0ddfa33362140feea997351b77.js",
    "context": {
      "path": "js/165d7b0ddfa33362140feea997351b77.js"
    }
  },
  {
    "path": "js/16df9ef05001a1741857bf99f5a5738f.js",
    "context": {
      "path": "js/16df9ef05001a1741857bf99f5a5738f.js"
    }
  },
  {
    "path": "js/2a85c11e395a8380b5915443e926b569.js",
    "context": {
      "path": "js/2a85c11e395a8380b5915443e926b569.js"
    }
  },
  {
    "path": "js/34be5330971fdbd18985525bd994b0aa.js",
    "context": {
      "path": "js/34be5330971fdbd18985525bd994b0aa.js"
    }
  },
  {
    "path": "js/35c5f9e096d4da33d2a62031daf14248.js",
    "context": {
      "path": "js/35c5f9e096d4da33d2a62031daf14248.js"
    }
  },
  {
    "path": "js/3d70953a848219e749fedc2cdb906675.js",
    "context": {
      "path": "js/3d70953a848219e749fedc2cdb906675.js"
    }
  },
  {
    "path": "js/3e940a33e44b65c1c0af8bb80a893530.js",
    "context": {
      "path": "js/3e940a33e44b65c1c0af8bb80a893530.js"
    }
  },
  {
    "path": "js/544d012df7acf9c3f0920f67c9e322b9.js",
    "context": {
      "path": "js/544d012df7acf9c3f0920f67c9e322b9.js"
    }
  },
  {
    "path": "js/55d3eccba73070ae6ee4dd7bdc017838.js",
    "context": {
      "path": "js/55d3eccba73070ae6ee4dd7bdc017838.js"
    }
  },
  {
    "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js",
    "context": {
      "path": "js/57d119d998d518b01f9d5ccb5e4d4c52.js"
    }
  },
  {
    "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js",
    "context": {
      "path": "js/67f6e2f99c3c3133e0dc669919fff5c5.js"
    }
  },
  {
    "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js",
    "context": {
      "path": "js/7045b35c5bd0e9c7cf59f1900eeeec41.js"
    }
  },
  {
    "path": "js/7260bab328b0ad74815a5efb377bcc67.js",
    "context": {
      "path": "js/7260bab328b0ad74815a5efb377bcc67.js"
    }
  },
  {
    "path": "js/893de96f1b6da546bd7c814964723eca.js",
    "context": {
      "path": "js/893de96f1b6da546bd7c814964723eca.js"
    }
  },
  {
    "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js",
    "context": {
      "path": "js/93e29fe348ddc9b71aba9c842adc18b8.js"
    }
  },
  {
    "path": "js/9455859483e31e4da0e28f10d0742c2a.js",
    "context": {
      "path": "js/9455859483e31e4da0e28f10d0742c2a.js"
    }
  },
  {
    "path": "js/9db10375d298678e53777a2347b87073.js",
    "context": {
      "path": "js/9db10375d298678e53777a2347b87073.js"
    }
  },
  {
    "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js",
    "context": {
      "path": "js/9f9b6e54f82a6bbc8bac9b89327024bc.js"
    }
  },
  {
    "path": "js/a2261649751fa61b606222c9b2ea3b80.js",
    "context": {
      "path": "js/a2261649751fa61b606222c9b2ea3b80.js"
    }
  },
  {
    "path": "js/b0bade6d42c2702ca85774296cc507c4.js",
    "context": {
      "path": "js/b0bade6d42c2702ca85774296cc507c4.js"
    }
  },
  {
    "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js",
    "context": {
      "path": "js/cd1ed86c1e7f06d985fd71bc10bd4b04.js"
    }
  },
  {
    "path": "js/cecb447a04bbe3e8982190dd6e697120.js",
    "context": {
      "path": "js/cecb447a04bbe3e8982190dd6e697120.js"
    }
  },
  {
    "path": "js/d80b370d82680fc786dcc943a327b9f2.js",
    "context": {
      "path": "js/d80b370d82680fc786dcc943a327b9f2.js"
    }
  },
  {
    "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js",
    "context": {
      "path": "js/df80c5cbcb312a9c7c0b2ebb6ac5f592.js"
    }
  },
  {
    "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js",
    "context": {
      "path": "js/f1e5dbc1ece900d164c2e9aa2d6a1386.js"
    }
  },
  {
    "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js",
    "context": {
      "path": "js/f3f02c438592c8e1bbe551f4dbbf4f5c.js"
    }
  },
  {
    "path": "office-spaces.html",
    "context": {
      "title": "Ikraft: Office Interior Design Company",
      "first_heading": "office spaces"
    }
  },
  {
    "path": "partner-with-us.html",
    "context": {
      "title": "Partner With Us \u2013 Modular Kitchen & Wardrobes Manufacturers",
      "first_heading": "PARTNER WITHUS"
    }
  },
  {
    "path": "portfolio.html",
    "context": {
      "title": "Ikraft- Best Company For Interior Design",
      "first_heading": "OurPORTFOLIO"
    }
  },
  {
    "path": "residential.html",
    "context": {
      "title": "Residential Interior Design Services",
      "first_heading": "RESIDENTIAL"
    }
  },
  {
    "path": "retail.html",
    "context": {
      "title": "Retail Shop Interior Designers",
      "first_heading": "RETAIL & RESTAURANTS"
    }
  },
  {
    "path": "services-backup.html",
    "context": {
      "title": "Best Interior Design Companies In India",
      "first_heading": "OurServices"
    }
  },
  {
    "path": "services.html",
    "context": {
      "title": "Best Turnkey Interior Contractors in Hyderabad | Ikraft",
      "first_heading": "OurServices"
    }
  }
]

Return only a JSON object mapping each path to its new basename (same extension). No other text.