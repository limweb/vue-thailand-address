<template lang="pug">
.typeahead-address-form
	.row
		.col
			typeahead-input(target='district', :label='subdistrictLabel')
		.col
			typeahead-input(target='amphoe', :label='districtLabel')
	.row
		.col
			typeahead-input(target='province', :label='provinceLabel')
		.col
			typeahead-input(target='zipcode', :label='zipcodeLabel')
</template>

<script lang="ts">
import Vue from 'vue';
import Component from 'vue-class-component';
import { Prop } from 'vue-property-decorator';

import store from '@/store';

import AddressEntry from '@/interface/AddressEntry';
import { loadDataSource } from '@/lib/datasource-utils';
import TypeaheadInput from './TypeaheadInput.vue';

@Component({
	name: 'address-form',
	components: {
		TypeaheadInput
	},
	store
})
export default class AddressForm extends Vue {
	// Props
	@Prop({ default: 'ตำบล/แขวง' })
	subdistrictLabel: string;
	@Prop({ default: 'อำเภอ/เขต' })
	districtLabel: string;
	@Prop({ default: 'จังหวัด' })
	provinceLabel: string;
	@Prop({ default: 'รหัสไปรษณีย์' })
	zipcodeLabel: string;

	// Hooks
	created() {
		let dataSource: AddressEntry[] = loadDataSource();
		this.$store.dispatch('updateDataSource', dataSource);
	}
}
</script>

<style lang="scss">
.typeahead-address-form {
	width: 100%;

	.row {
		display: block;

		&:not(:first-child) {
			margin-top: 20px;
		}
		.col {
			display: inline-block;
			width: 49%;

			&:not(:last-child) {
				margin-right: .5%;
			}
			&:not(:first-child) {
				margin-left: .5%;
			}
		}
	}
}
</style>
