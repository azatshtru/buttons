<script>
    export let buttonIcon = "fa-heart";
    export let hueRotation = '0deg';
</script>

<div class="container">
    <button class="heart" style="filter: hue-rotate({hueRotation});">
        <i class="fa-solid {buttonIcon} white"></i>
    </button>
</div>

<style>

    .container {
        display: flex;
        height: 100%;
        justify-content: center;
        align-items: center;
    }

    .heart {
        width: 150px;
        height: 150px;
        background: linear-gradient(180deg, #fbfbfb, #e5d2c8);
        border: 0px solid #e2ddda;
        border-radius: 30px;
        overflow: hidden;
        box-shadow: 0px 20px 60px #af978f;
        transition: box-shadow 0.3s ease, scale 0.3s ease;
    }

    .heart::before{
        content: '';
        position: absolute;
        width: 105px;
        height: 105px;
        transform: translate(-50%, -50%);
        background: linear-gradient(180deg, #e5d9d4, #fdfdfa);
        border-radius: 30px;
        box-shadow: inset 0px 20px 10px #f0e6e4;
        border-block: 1px solid #c6ab9e;
        transition: box-shadow 0.3s cubic-bezier(0.075, 0.82, 0.165, 1);
    }

    .heart i {
        position: absolute;
        color: #e6d8d2;
        font-size: 2.5em;
        text-shadow: 0px -2px #d5c7bf;
        -webkit-background-clip: text;
        -moz-background-clip: text;
            background-clip: text;
        transform: translate(-50%, -50%);

        transition: color 0.3s cubic-bezier(0.075, 0.82, 0.165, 1);
    }

    .heart:hover {
        box-shadow: 0px 10px 30px #af978f;
    }

    .heart:active {
        box-shadow: 0px 1px 1px #af978f;
        scale: 0.92;
    }

    .heart:active::before{
        box-shadow: inset 0px 80px 5px #f0e6e4;
    }

    .heart:active i {
        color: white;
    }

</style>