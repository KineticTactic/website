<navbar>
    <ul>
        <li>
            <a href="index.php">Projects</a>
        </li>
        <!-- <li class="seperator">•</li> -->
        <li>
            <a href="index.php">About</a>
        </li>
        <li>
            <a href="index.php">Contact</a>
        </li>
    </ul>
</navbar>

<style>
    ul {
        list-style-type: none;
        margin: 0;
        padding: 0;
        overflow: hidden;
        display: flex;
        justify-content: center;
    }

    li {
        /* margin: 0 1rem; */
    }

    li + li::before {
        content: "•";
        color: #9c9dbd;
    }

    li a {
        display: inline-block;
        color: #9c9dbd;
        text-align: center;
        text-decoration: none;
        font-family: Poppins, sans-serif;
        font-weight: 300;
        margin: 0 1rem;
    }
</style>
