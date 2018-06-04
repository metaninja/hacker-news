<template>
    <div>
        <header class="app-bar-top">
            <h1>
                <a href="#" class="logo">
                    <i class="material-icons">menu</i>
                </a>
                Hacker News
            </h1>
            <div class="app-bar-top__right">
                <a href="#"><i class="material-icons">account_circle</i></a>
            </div>
        </header>
        <nav class="app-bar-top-nav">
            <ul class="tabs">
                <li class="tabs__tab tabs__tab--active"><a href="/">New</a></li>
                <li class="tabs__tab"><a href="/comments">Comments</a></li>
                <li class="tabs__tab"><a href="/show">Show</a></li>
                <li class="tabs__tab"><a href="/ask">Ask</a></li>
                <li class="tabs__tab"><a href="/jobs">Jobs</a></li>
            </ul>
        </nav>
    </div>
</template>

<script>
    export default {
        name: "AppBarTop"
    }
</script>

<style scoped>
.app-bar-top-nav {
    margin-top: 60px;
}
</style>