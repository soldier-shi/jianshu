<template>
    <div class="CoArticle">
    	<myheader></myheader>
    	<div class="my-container content">
            <div class="row">
            	<div class="col-1"></div>
            	<div class="col-9 main">
            		<img width="100%" src="../assets/img/collect-note.png"/>
            		<ul class="note-list">
            			
            		</ul>
            	</div>
            </div>
        </div>
    </div>
</template>

<script>
	import myheader from '../components/myHeader.vue'
    export default {
        name: "collection-article",
        components:{
        	myheader
        }
    }
</script>

<style scoped>
	.content .row{
		padding-top: 30px;
	}
	.content .row .main img{
		margin-bottom: 30px;
		min-height: 100px;
		border-radius: 6px;
	}
	@media (max-width: 1080px) {
        .CoArticle .content{
            width: 750px!important;
        }
    }
    @media (max-width: 750px) {
        .CoArticle{
            overflow: hidden;
        }
    }
</style>