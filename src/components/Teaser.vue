<template>
	<div class="teaser">

		<h1 v-if="showTitle" class="author__site-title">
			TEASER
		</h1>

	

	</div>
</template>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<script>
export default {
	props: ['showTitle']
}
</script>

<style lang="scss">
.teaser {
	margin: 0 auto;
	max-width: 500px;
	text-align: center;
	padding-bottom: calc(var(--space) / 2);
}
</style>
