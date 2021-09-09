# MACK http://cwaller.altervista.org/TAP/websiteSkeleton.html
<!DOCTYPE html>
<html>
<head>
	<title>My Page</title> <!---Step 1: Create a title--->
    <!--Online CSS files for styling the page-->
	<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/font-awesome/4.6.3/css/font-awesome.min.css">
	<link rel="stylesheet" type="text/css" href="https://cdnjs.cloudflare.com/ajax/libs/bulma/0.3.1/css/bulma.min.css">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
	<style>
      html, body{font-size:16px;color: #ffffff;background-color: #ff3333; /*Optional Step: Change top tab color*/}

      /*Step 2: Change the color of these sections*/
      .section-1 {background-color: #ffcc00;}
      .section-2 {background-color: green;}
      .section-3 {background-color: #1a8cff;}
      
      /*Don't Touch Please - Scroll to About*/
      a {color: blue;}
      section{padding-top: 3rem;padding-bottom: 3rem;}
      a.nav-item {color: #dfdfdf;}
      a.nav-item:hover {color: #fff;}
      .avatar{height:200px;border-radius: 50%;}
      .intro-description{padding-top: 1rem;}
      .box {background-color: transparent;border: 2px solid rgba(7, 59, 79, 0.5);}
      .title {color: #fff;text-align: center;margin-bottom: 2rem;}
      .intro {text-align: center;width: 80%;margin: 0 auto;}
      .void-background {background-color: transparent; }
      .quote-box {text-align: center;}
      @media screen and (max-width: 768px) {.nav-menu {background-color: #063647;}}
    </style>
</head>
	<body>
		<!-- Navbar. KEEP SCROLLING :) -->
		<nav class="nav container void-background">
			<div class="nav-center">
				<a href="http://instagram.com/" class="nav-item"><span class="icon"><i class="fa fa-instagram"></i></span></a>
				<a href="http://facebook.com/" class="nav-item"><span class="icon"><i class="fa fa-facebook"></i></span></a>
				<a href="https://twitter.com/" class="nav-item"><span class="icon"><i class="fa fa-twitter"></i></span></a>				
			</div>
		</nav>
				
		<!-- About Me -->
          <section id="about" class="section section-1">
              <h3 class="title is-3">About Me</h3><center>
                  <!---Step 3: Add an image by src--->
                  <img class="avatar" src="https://metiza.com/wp-content/uploads/2017/01/how-to-become-morning-person.jpg"><br/>
              </center><p class="intro">
                  I love to play volleyball and eat icecream! I am a Senior in college getting a degree in Digital Media. :)
              </p>
          </section>

        <!-- Quote -->
          <section id="quotes" class="section section-2">
                  <h3 class="title is-3">Quote of the Day</h3>
                  <div class="quote-box"><p id="quote">"Quote goes here..."</p><small id="author">- Author</small></div>
          </section>	

          <!-- Content -->
          <section  id="contents" class="section section-3"><center>
              <h3 class="title is-3">Content</h3>
                  <p class="intro">
                      This link can take you to <a href="https://google.com">google.</a><br/>
                      Here's a pretty picture:
                  </p><br/>
                  <img src="https://th.bing.com/th/id/R.609395c25e91318f66045ba76a92ed20?rik=ENFe%2bpahJmzr%2bw&pid=ImgRaw&r=0" alt="flowers" height="800" width="800"><br/>
                  <p>Now a table:</p>
                  <table style="width:50%;">
                    <tr>
                      <th>Column Header 1</th>
                      <th>Column Header 2</th>
                      <th>Column Header 3</th>
                    </tr>
                    <tr>
                      <td>Row 1 - Column 1</td>
                      <td>Row 1 - Column 2</td>
                      <td>Row 1- Column 3</td>
                    </tr>
                    <tr>
                      <td>Row 2 - Column 1</td>
                      <td>Row 2 - Column 2</td>
                      <td>Row 2 - Column 3</td>
                    </tr>
                  </table>
          </center></section>
		
		<!-- Scripts (Javascript for Quote Generator in Section 2) -->
        <script>
          const quote = document.querySelector("#quote");
          const author = document.querySelector("#author");
          window.onload = getQuote;
           function getQuote() {
            fetch("http://quotable.io/random")
              .then(res => res.json())
              .then(data => {
              quote.innerHTML = `"${data.content}"`;
              author.innerHTML = data.author;
            })
          }
    	</script>
	</body>	
</html>
