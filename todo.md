Radar {
    timestamp, 
    dual: bool
    limit: int
    roadId: int,
    id: int
}

Speed {
    min: int,
    max: int,
    average: int,
}

Road {
    stats: StatPerRoad.id[],
    speed: Speed
    radars: Radar []
}

StatPerRoad {
    start: timestamp
    end: timestamp
    speed: Speed
    radar: null | Radar.id,
    speed_limit: int,
    id
}

Route {
    roads: StatPerRoad.id[]
    start: timestamp,
    end: timestamp
    speed: Speed,
    id
}


Fuel {
    timestamp,
    price: float, (euros per liters)
    contentBeforeFueling: float, (liters)
    value: float (liters)
}

General {
    fuel: fuel.id[],
    km: float,
    driving_time: float (msg)
}