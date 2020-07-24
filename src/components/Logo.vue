<template>
  <g-link class="logo" to="/">
  	<svg class="logo__image" width="42" height="42" viewBox="0 0 42 42" fill="none" xmlns="http://www.w3.org/2000/svg">
		<mask id="mask0" mask-type="alpha" maskUnits="userSpaceOnUse" x="0" y="0" width="40" height="40">
		<circle cx="20" cy="20" r="20" class="logo_bg"/>
		</mask>
		<g mask="url(#mask0)">
		<circle cx="20" cy="20" r="20" class="logo_bg"/>
		<path class="logo_fill"  fill-rule="evenodd" clip-rule="evenodd" d="M35.8454 29.7591C37.5354 26.9523 38.5075 23.6643 38.5075 20.1493C38.5075 9.84543 30.1546 1.49254 19.8508 1.49254C13.194 1.49254 7.35149 4.97886 4.04954 10.2252C2.24041 8.98179 0.049235 8.25403 -2.31192 8.25403V39.7753H8.93252V35.2792C10.2826 36.2552 11.7686 37.0549 13.3565 37.6446L13.3565 39.7753H35.8454L35.8454 29.7591ZM35.8454 29.7591L35.8454 19.4985C35.8454 13.2883 30.8111 8.25402 24.601 8.25402C18.3908 8.25402 13.3565 13.2883 13.3565 19.4985L13.3565 37.6446C15.379 38.3956 17.5669 38.806 19.8508 38.806C26.6395 38.806 32.5814 35.18 35.8454 29.7591ZM1.19404 20.1493C1.19404 26.376 4.24449 31.8903 8.93252 35.2792V19.4985C8.93252 15.6495 6.99864 12.2522 4.04954 10.2252C2.2405 13.0996 1.19404 16.5022 1.19404 20.1493Z" />
		<circle cx="20" cy="20" r="20" stroke-width="1.5"/>
		</g>
	</svg>

    <span class="logo__text">{{ $static.metadata.siteName }}</span>
  </g-link>
</template>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<style lang="scss">
.logo {
  text-decoration: none;
  color: var(--body-color) !important;
  font-size: 0.9em;
  display: flex;
  align-items: center;

  &__image {
		.logo_fill {
			fill: var(--logo-color);
			
		}
		stroke: var(--logo-fill-color); 
		.logo_bg {
			fill: var(--logo-fill-color); 
		}
		&:hover {
			.logo_bg {
				fill: var(--logo-hover-color); 
				transition: all .6s ease;
			}
			stroke: var(--logo-hover-color); 
			transition: all .6s ease;
		}	
  }

//   &__image {
//     vertical-align: middle;
//     border-radius: 99px;
//     height: 40px;
//     width: 40px;
// 	margin-right: 0.5em;
// 	background-image: url('/images/logo.svg');
// 	background-size: 40px;
// 	background-repeat: no-repeat;
//   }

  &__text{
	  margin-left: 10px;
  }
}

</style>
