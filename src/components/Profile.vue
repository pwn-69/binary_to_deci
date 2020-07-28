<template>
    <div>
        <b-navbar type="dark" variant="dark">
            <b-navbar-nav>
                <b-nav-item href="/">Converter</b-nav-item>

                <b-nav-item-dropdown text="About" right>
                <b-dropdown-item href="#/profile">Profile</b-dropdown-item>
                <b-dropdown-divider></b-dropdown-divider>
                <b-dropdown-item href="#">Resources</b-dropdown-item>
                </b-nav-item-dropdown>
            </b-navbar-nav>
        </b-navbar>
        <br>
        <br>
            <div>
                <b-card bg-variant="dark" text-variant="white" style="width:50%" class="ml-4">
                    <b-card-header>
                         <b-avatar size="6rem">
                             <img src="../assets/pwn.jpg" alt="me" style="width:130px">
                         </b-avatar>
                    </b-card-header>
                    <b-card-text>
                        <p><strong>Phyo Wai Nyunt</strong></p>
                        <p><strong>Third Year Computer Science Student</strong></p>
                    </b-card-text>
                    <br>
                    <b-card-text>
                    <p><strong>Get in touch...</strong></p>
                    <b-button bg-variant="outline-white" href="https://www.linkedin.com/in/phyo-wai-nyunt-56ba55195/"><b-icon icon="bell"></b-icon></b-button>
                    </b-card-text>
                </b-card>
            </div>
    </div>
</template>

<script>
    export default {
        name: 'Profile' 
    }
</script>