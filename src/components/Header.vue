<template>
    <header>
        <h1>Vue JS</h1>
        <nav>
            <a href="#">Home</a>
            <a href="#">About</a>
            <a href="#">Projects</a>
            <a href="#">Contact</a>
        </nav>
    </header>
</template> 


<style scoped>

    header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 10px 20px;
        background-color: royalblue;
    }

    header nav {
        display: flex;
        align-items: center;
        gap: 10px;
    }

    header nav a {
        color: black;
        text-decoration: none;
    }

    header nav a:hover {
        color: white;
    }
</style>