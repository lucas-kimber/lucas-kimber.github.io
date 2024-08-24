<template>
    <div class="brand">
        <p class="lg-first">Lucas</p>
        <p class="lg-last">Kimber</p>
        <div class="lg-deco"></div>
        <marquee direction="up" behavior="alternate" height="18px" truespeed scrolldelay="500" class="lg-sub">Computer Scientist<br/>Zootopia Enjoyer<br/>Playboy Philathropist</marquee>
    </div>
</template>
<style lang="scss">
.brand {
    color: white;
    // background-color: rgba(255,255,255,0.2);
    width: 400px;
    display: inline-block;
    margin-bottom: 20px;
    position: relative;
}
.lg-first, .lg-last, .lg-deco, .lg-sub {
    margin: 0;
    line-height: 1em;
}

.lg-first {
    font-weight: 200;
    font-size: 30px;
}
.lg-last {
    font-weight: 700;
    font-size: 50px;
    margin-left: 50px;
}
.lg-deco {
    width: 230px;
    height: 3px;
    background-color: var(--accent);
    box-shadow: 0 0 5px 0 var(--shadow);
    margin: 7px 7px 12px 50px;

}

.lg-sub {
    letter-spacing: 1px;
    line-height: 1.4rem;
    margin-left: 50px;
}

@media screen and (max-width: 340px){
    .lg-first {
        margin-left: 50px;
    }
    .brand {
        text-align: left;
    }
}


</style>