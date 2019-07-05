<template>
  <div>
    <b-navbar toggleable="lg" type="dark" variant="info">
        <b-navbar-brand href="#">Vue | Trello</b-navbar-brand>
        
        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

        <b-collapse id="nav-collapse" is-nav>
            <b-navbar-nav class="ml-auto">
                <b-nav-item href="#">Home</b-nav-item>
                <b-nav-item class="mr-sm-4" href="#">My Boards</b-nav-item>
                <b-nav-form>
                    <b-form-input size="sm" class="mr-sm-2" placeholder="Search..."></b-form-input>                    
                </b-nav-form>                
            </b-navbar-nav>

            <!-- Right aligned nav items -->
            <b-navbar-nav class="ml-auto">                
                <b-nav-item-dropdown no-caret right>
                    <template slot="button-content">
                        <b-button class="showMain">+</b-button>
                        <b-button class="showSub">Create...</b-button>
                    </template>                    
                    <b-dropdown-item href="#">Create Board...</b-dropdown-item>      
                    <b-dropdown-divider></b-dropdown-divider>              
                    <b-dropdown-item href="#">Create Team...</b-dropdown-item>  
                    <b-dropdown-divider></b-dropdown-divider>                  
                    <b-dropdown-item href="#">Create Business Team...</b-dropdown-item>                    
                </b-nav-item-dropdown>
                <b-nav-item-dropdown no-caret right>
                    <template  slot="button-content">
                        <b-button class="showMain" pill>{{ getInitials }}</b-button>
                        <b-button class="showSub">My Profile...</b-button>
                    </template>
                    <b-dropdown-item href="#">{{ getFullName }} (@{{ username }})</b-dropdown-item>    
                    <b-dropdown-divider></b-dropdown-divider>                
                    <b-dropdown-item href="#">Profile</b-dropdown-item>                    
                    <b-dropdown-item href="#">Cards</b-dropdown-item>                    
                    <b-dropdown-item href="#">Settings</b-dropdown-item> 
                    <b-dropdown-divider></b-dropdown-divider>   
                    <b-dropdown-item href="#">Help</b-dropdown-item>                    
                    <b-dropdown-item href="#">Shortcuts</b-dropdown-item>                    
                    <b-dropdown-item href="#">Change Language</b-dropdown-item>  
                    <b-dropdown-divider></b-dropdown-divider>                   
                    <b-dropdown-item href="#">Logout</b-dropdown-item>                     
                </b-nav-item-dropdown>
            </b-navbar-nav>
        </b-collapse>
    </b-navbar>
  </div>
</template>

<script>
export default {
  name: 'NavBar',
  props: {
    firstName: String,
    lastName: String,
    username: String
  },
  computed: {
    getFullName: function() {
        return `${this.firstName} ${this.lastName}`                 
    },
    getInitials: function() {
        return this.firstName.charAt(0).toUpperCase() + this.lastName.charAt(0).toUpperCase() 
    }
  }
}
</script>

<style scoped>
@media (min-width: 992px) { 
    .showMain {
        display: unset !important;
    }
    .showSub {
        display: none;
    }
}

@media (max-width: 992px) { 
    .showMain {
        display: none;
    }
    .showSub {
        display: unset !important;
    }
}
</style>
