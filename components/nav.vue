<template>
    <div>
        <ul class="nav-menu">
            <li><NuxtLink to="/education">Education</NuxtLink></li>
            <li class="sep">|</li>
            <li><NuxtLink to="/skills">Skills</NuxtLink></li>
            <li class="sep">|</li>
            <li><NuxtLink to="/employment">Employment</NuxtLink></li>
        </ul>
    </div>
</template>
<style lang="scss">
.nav-menu {
    list-style: none;
    display: flex;
    justify-content: space-between;
    padding-right: 15px;
    border-top: 1px solid #4b4b4b;
    border-bottom: 1px solid #4b4b4b;
    padding: 5px 0 5px 0;

    .sep {
        opacity: 0.2;
    }

    a {
        font-size: 25px;
        color: white;
        text-decoration: none;

        &.router-link-active {
            text-decoration: underline;
        }
    }
}

@media screen and (max-width: 768px) {
    .nav-menu {
        padding-right: 0;
        li {
            a {
                font-size: 18px;
            }
        }
    }
}

</style>