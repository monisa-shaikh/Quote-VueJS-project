<template>
    <div class="row">
        <div class="col-sm-12">
            <h2>Progress Bar</h2>
            <div class="progress">
                <div class="progress-bar" role="progressBar" aria-valuenow="60" aria-valuemin="0" aria-valuemax="100 "
                :style="{width: (quotesCount / maxQuotes ) * 100 +'%'}">
                    {{ quotesCount }} /{{ maxQuotes }}
                </div>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    props:['quotesCount','maxQuotes']
}
</script>