<template>
  <div class="text-center footer">
    <v-bottom-sheet v-model="sheet">
      <template v-slot:activator="{ on }">
        <div class="nav-bar">
          <nav><a href="/">Articles</a></nav>
          <v-btn v-on="on">Contact Me</v-btn>
          <nav><a href="/about">About Me</a></nav>
        </div>
      </template>
      <v-sheet class="text-center" height="500px">
        <v-btn
          class="foot-close-btn"
          @click="sheet = !sheet"
        >X</v-btn>
        <div class="inner-nav-bar">
					<h4 class="title">Contact Me</h4>
					<div>
						<p>
							<span>Email:- </span>
							<span>13kmlraj@gmail.com</span>
						</p>
						<p>
							<span>Contact No.:- </span>
							<span>+91 8674837392</span>
						</p>
						<div class="icon-container">
							<a href="https://www.linkedin.com/in/kml1326/"><v-icon large color="#0278e1" class="icon">mdi-linkedin</v-icon></a>
							<a href="https://github.com/kml1326"><v-icon large color="#363f47" class="icon">mdi-github-circle</v-icon></a>
							<a href="https://twitter.com/_kml1326"><v-icon large color="#76bfff" class="icon">mdi-twitter</v-icon></a>
							<a href="https://www.instagram.com/_kml1326/"><v-icon large color="#df1e8d" class="icon">mdi-instagram</v-icon></a>
						</div>
					</div>
        </div>
      </v-sheet>
    </v-bottom-sheet>
  </div>
</template>

<script>
export default {
	data() {
		return {
			sheet: false
		}
	}
}
</script>

<style lang="scss" scoped>
  .footer {
    position: fixed;
    bottom: 0;
    display: block;
    width: 100%;
    background: #fff;
    padding: 10px 0 50px 0;
    border-top-left-radius: 20px;
    border-top-right-radius: 20px;
  }
  .v-btn:not(.v-btn--round).v-size--default {
    border-radius: 50%  ;
    padding: 10px;
    min-height: 50px;
    min-width: 50px;
  }

  .nav-bar {
    width: 80%;
    margin: 0 auto;
    display: flex;
    justify-content: space-around;
    align-items: center;
  }

	.title {
		font-size: 20px;
    margin-bottom: 20px;
	}

	.inner-nav-bar {
		margin: 30px auto;
    width: 80%;
	}

	.icon-container {
		a {
			text-decoration: none;
		}
	}

	.icon {
		margin: 20px;
		&:hover {
			box-shadow: 1px 2px 2px 2px #a19b9b33;
			transition: all 0.2s .1s;
		}
	}
</style>