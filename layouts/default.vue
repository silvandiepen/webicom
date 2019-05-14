<template>
	<div class="layout layout-default" :class="[`page--${pageName}`]">
		<layout-header />
		<nuxt />
		<layout-footer />
	</div>
</template>

<script>
import LayoutHeader from '~/components/layout/header.vue';
import LayoutFooter from '~/components/layout/footer.vue';

export default {
	components: {
		LayoutHeader,
		LayoutFooter
	},
	data() {
		return {
			pageName: null
		};
	},

	watch: {
		$route() {
			this.pageName = this.getPageName();
		}
	},
	created() {
		this.pageName = this.getPageName();
	},
	methods: {
		getPageName() {
			let pathName = this.$route.params.pathMatch;
			if (pathName) {
				return pathName;
			} else if (this.$route.name) {
				return this.$route.name;
			} else {
				return 'index';
			}
		}
	}
};
</script>
