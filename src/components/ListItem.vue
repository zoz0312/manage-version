<template>
	<v-container>
		<v-layout
			wrap
			>
			<v-card class="mx-auto" width='100%'>
				<v-simple-table dense class='tbl-info pt-3'>
					<template v-slot:default>
						<tr class='tr-version'>
							<th width='20%'>버전</th>
							<td>{{ propsdata.version }}</td>
						</tr>
						<tr>
							<th width='20%'>카테고리</th>
							<td>{{ propsdata.category }}</td>
						</tr>
						<tr>
							<th width='20%'>적용범위</th>
							<td>{{ propsdata.apply_range }}</td>
							<th width='20%'>작성일</th>
							<td>{{ propsdata.date }}</td>
						</tr>
					</template>
				</v-simple-table>
				<v-card-text>
					<div class='main-desc'>
						{{ propsdata.main_desc }}
					</div>
					<div class='sub-desc'>
						{{ propsdata.sub_desc }}
					</div>
				</v-card-text>
				<v-card-actions>
					<v-btn text color="deep-purple accent-4">
						SQL : {{ propsdata.attach_name }}
					</v-btn>
				</v-card-actions>
			</v-card>
		</v-layout>
	</v-container>
</template>

<script>
export default {
	props: ['propsdata'],
  name: 'ListItem',

  data: () => ({
  }),
};
</script>
<style scope>
.main-desc {
	margin-bottom: 1rem;
	font-size: 1.7rem;
	color: #333333;
}
.sub-desc {
	font-size: .8rem;
	color: #333333;
}
.tbl-info .tr-version td {
	font-size: 1rem !important;
	color: #B71C1C !important;
}
.tbl-info th {
	font-size: 1rem !important;
}
.tbl-info td {
	font-size: .8rem !important;
}
.tbl-info th,
.tbl-info td {
	color: #333333 !important;
}
</style>
