SpiterFlagEvent



1.can get Player,check,type,info,vl,maxvl,time;

2.How to use:

   @EventHandler
    public void onJoin(SpiterFlagEvent event) {
        Player player = event.getPlayer();
    
        String check = event.getcheck();
       String type = event.getype();
       String info;
       int vl;
      int maxvl;
      long timestamp;
    }

    
