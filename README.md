```rust
//! From a homelab to a data center.

#![forbid(unsafe_code)]

pub const AUTHOR: &str = "Comugi";

type Record = (&'static str, &'static str, &'static str);

pub mod homelab {
    // Hostname, Processor, Memory (GiB)
    pub const COMPUTE: &[(&str, &str, u16)] = &[
        ("node01", "Core i7-8700",     48),
        ("node02", "Core i7-2600",     16),
        ("node03", "Xeon E5-2640 v4",  64),
    ];

    pub const NETWORK: &[(&str, &str)] = &[
        ("WAN",      "10G-ONU"),
        ("Gateway",  "XG-200KI"),
        ("Isolated", "Archer AX23V / OpenWrt"),
    ];

    // TODO: Integrate Catalyst 3650-24TS-S.
}

pub mod projects {
    use super::Record;

    pub const HISTORY: &[Record] = &[
        ("ALLIANCE-PLANET", "Minecraft Server",         "2025.04–2025.10"),
        ("MugicBot",       "HRIR / 9.1.4 Spatial Audio", "2026.03–Present"),
    ];
}

pub mod communities {
    use super::Record;

    pub const AFFILIATIONS: &[Record] = &[
        ("Alliance",         "Former Technical Lead", "2025.04–2025.10"),
        ("SHIN DATA CENTER", "Member",                "2024.10–Present"),
        ("Tsukuyomi",        "IT Systems Lead",        "2026.04–Present"),
        ("KuronekoServer",   "Artifactor Developer",   "2026.04–Present"),
        ("Luna Project",     "Yuzuki Developer",       "2026.04–Present"),
    ];
}

pub mod experience {
    pub const DOMAINS: &[&str] = &[
        "Access Control & ACL Management",
        "Core Network Architecture & Redundancy",
        "Disaster Prevention IP Infrastructure",
        "IPsec VPN & LTE Integration",
        "Surveillance Network Infrastructure",
    ];

    pub const PLATFORMS: &[&str] = &[
        "Cisco Catalyst / Nexus",
        "NEC IX / QX / WA",
    ];
}
