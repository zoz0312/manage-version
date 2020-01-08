<template>
	<v-container>
		<v-layout
			wrap
			>
			<v-card class="mx-auto" width='100%'>
				<div class='div-input'>
					<v-text-field label="Version" class='input-text' :value='version'/>
					<v-dialog
						ref="dialog"
						v-model="modal"
						:return-value.sync="date"
						persistent
						width="290px">
						<template v-slot:activator="{ on }">
							<v-text-field v-model="date" label="Picker in dialog"
								readonly
								v-on="on"
							></v-text-field>
						</template>
						<v-date-picker v-model="date" scrollable>
							<v-spacer></v-spacer>
							<v-btn text color="primary" @click="$refs.dialog.save(date)">OK</v-btn>
						</v-date-picker>
					</v-dialog>
					<v-text-field label="제목" class='input-text' :value='main_desc'/>
					<v-textarea clearable 
						label="상세설명"
						:value='sub_desc'></v-textarea>
				</div>
				<span class='span-title title blue--text text--darken-3'>파일첨부</span>
				<div class='div-input'>
					<v-file-input
						v-model="files"
						placeholder="Upload your documents"
						label="File input"
						multiple
						prepend-icon="mdi-paperclip">
						<template v-slot:selection="{ text }">
							<v-chip small label color="primary">
								{{ text }}
							</v-chip>
						</template>
					</v-file-input>
				</div>
				<v-card-actions>
					<v-btn text color="deep-purple accent-4">
						작성하기
					</v-btn>
				</v-card-actions>
			</v-card>
		</v-layout>
	</v-container>
</template>

<script>
export default {
  name: 'PostCard',

  data: () => ({
		date: new Date().toISOString().substr(0, 10),
		modal: false,
		version: '',
		main_desc: '',
		sub_desc: '',
		files: null,
  }),
};
</script>

<style scope>
.div-input {
	padding: 1rem 1rem;
}
.input-text {
	margin-bottom: -1rem;
}
.span-title {
	padding-left: 1rem;
}
</style>
