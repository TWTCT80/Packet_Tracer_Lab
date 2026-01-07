# Nätverkssäkerhet – Projektarbete (Cisco Packet Tracer)

## Översikt

Detta repository innehåller ett grupprojekt genomfört inom kursen **Nätverkssäkerhet (40 yhp)** på utbildningen **IT- och cybersäkerhetsspecialist (CS25)** vid Frans Schartaus Handelsinstitut.

Projektets syfte är att designa, implementera och dokumentera en säker nätverksinfrastruktur för ett fiktivt företag med två geografiskt separerade siter: **Stockholm** och **Göteborg**. Nätverket är uppbyggt och simulerat i **Cisco Packet Tracer** och omfattar både funktionell konfiguration och säkerhetshärdning.

## Projektmål

- Designa ett segmenterat företagsnätverk med flera säkerhetszoner  
- Implementera VLAN, subnät och IP-plan enligt givna krav  
- Upprätta säker kommunikation mellan siter via virtuell tunnel  
- Konfigurera routing, DHCP och grundläggande nätverkstjänster  
- Implementera och verifiera säkerhetsåtgärder på flera OSI-lager  
- Simulera och analysera en säkerhetsincident samt motåtgärder  

## Nätverksdesign (sammanfattning)

- Två siter:  
  - Stockholm: `10.0.1.0/24`  
  - Göteborg: `172.16.2.0/24`
- Segmentering med VLAN:
  - Kontor  
  - Guest  
  - Admin  
  - Native VLAN  
  - Blackhole VLAN
- Routing on a Stick (ROAS) på edge-routrar
- GRE-tunnel mellan siter över ISP-nät
- Central server med begränsad åtkomst
- Identisk topologi på båda siter

## Säkerhetsfokus

Projektet innehåller dokumentation och implementation av flera säkerhetsåtgärder, bland annat:

- VLAN-segmentering och isolering av guest-nät
- ACL:er för trafikbegränsning mellan zoner
- SSH-härdning (endast SSHv2, begränsad åtkomst)
- Inaktivering av osäkra tjänster och protokoll
- Port-security på accessportar
- Blackhole VLAN för okänd eller obehörig trafik
- Säkerhetsåtgärder kopplade till flera OSI-lager

Utöver implementationen innehåller projektet även separata analyser av identifierade **attackvägar** och hur dessa kan motverkas genom korrekt nätverksdesign och konfiguration.

## Innehåll i detta repository

- **Packet Tracer-fil (.pkt)**  
  Komplett simulerad nätverksmiljö enligt projektkraven.

- **PDF-dokumentation**  
  - Nätverksdiagram med topologi och IP-plan  
  - Beskrivning av VLAN, routing och tunnlar  
  - Dokumenterade attackvägar och säkerhetsåtgärder  
  - Tester och verifiering av funktionalitet och säkerhet  

- **Övrigt material**  
  Kompletterande filer som använts under projektets genomförande.

## Verktyg och teknik

- Cisco Packet Tracer  
- Cisco IOS (router- och switchkonfiguration)  
- GRE-tunnling  
- VLAN, ACL, DHCP och statisk routing  
- Grundläggande nätverkssäkerhet  

## Avgränsningar

Projektet är genomfört i en simulerad miljö. Fokus ligger på nätverksdesign, säkerhetsprinciper och korrekt konfiguration, inte på prestanda eller drift i produktionsmiljö.

## Kontext

Detta arbete är en del av en examinerande gruppuppgift inom kursen **Nätverkssäkerhet** och är avsett att visa förståelse för både praktisk nätverkskonfiguration och säkerhetsrelaterade designval.
