# Tweaked SonicPi Tilborg 2 Example

```ruby
live_loop :beat  do
  with_fx  :level, amp: 12 do
    sample  :bd_boom
    sleep 0.2019 * 4
  end
end

live_loop :happy_new_year, sync: :beat do
  with_fx :reverb, room: 1 do
    use_synth :pretty_bell
    use_random_seed 2019
    notes = (scale 20 + 19, :minor_pentatonic, num_octaves: 7).take(24)
    52.times do
      play notes.choose, release: 0.2019, amp: rand + 0.2019, cutoff: rrand(20, 19), amp: 4
      sleep 0.2019
    end
  end
end
```
