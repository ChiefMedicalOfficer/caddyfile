# Save as Caddyfile - no file extension

domain.duckdns.org {
    root c:\caddy 
	proxy /tautulli 192.168.1.234:8181 { 
        transparent
    }
    timeouts {
      read none
      write none
      header none
    }
}

qbittorrent.domain.duckdns.org {
	proxy / 127.0.0.1:9999 {
		header_upstream X-Forwarded-Host {host}:9999
		header_upstream -Origin
		header_upstream -Referer
	}
}

dog.domain.duckdns.org {
    proxy / 192.168.1.231 {
	
	   transparent
	} 
}

piwigo.domain.duckdns.org {
    
    proxy / 192.168.1.234:9091 {
    
        transparent
    }		
}	
sonarr.domain.duckdns.org {
	proxy / 192.168.1.234:8989 {
		transparent
	}	
}

radarr.domain.duckdns.org {
	proxy / 192.168.1.234:7878 {
		
		transparent
	}	
}

bookstack.domain.duckdns.org {
	
	proxy / 192.168.1.234:8585 {
		
		transparent
	}
}

deluge.domain.duckdns.org {
    proxy / localhost:8112 {
	
		transparent
	}
}

portainer.domain.duckdns.org {
    proxy / localhost:9000 {
	
		transparent
	}
}

syncthing.domain.duckdns.org {
    proxy / localhost:8384 {
	
		transparent
	}	
}

jellyfin.domain.duckdns.org {
    proxy / localhost:8096 {
	
		transparent
	}	
}

netdata.domain.duckdns.org {
	proxy / localhost:19999 {
	
		transparent
	}
}
